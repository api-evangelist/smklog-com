# auth.md — SMKlog Quote API

Agent registration and authentication for the SMKlog quote service.

The API works without credentials: rate quotes and payment sessions are open,
rate limited per client per hour. Credentials exist for one reason — an agent
whose legitimate traffic outgrows the anonymous limits gets its own hourly
bucket at its own size.

## Registration

There is no self-service registration yet. Write to info@smklog.com with what
you are building and the volume you expect; credentials are issued manually and
the secret is shown exactly once.

## Getting a token

OAuth 2.0 client_credentials against the token endpoint from
`/.well-known/oauth-authorization-server`:

    POST https://quote-api.smklog.com/oauth/token
    Content-Type: application/x-www-form-urlencoded

    grant_type=client_credentials&client_id=...&client_secret=...

`client_secret_basic` works too. The answer carries an opaque bearer token,
valid for one hour, scope `quote`.

## Using it

    Authorization: Bearer smk_at_...

on `POST /quote`. An expired or revoked token gets 401 `invalid_token` — the
request is never silently downgraded to anonymous limits, so failures are loud.

## agent_auth

```json
{
  "agent_auth": {
    "register_uri": "mailto:info@smklog.com",
    "registration_methods": ["manual_email"],
    "identity_types": ["service"],
    "credential_types": ["client_secret"],
    "resource": "https://quote-api.smklog.com",
    "authorization_servers": ["https://quote-api.smklog.com"],
    "scopes_supported": ["quote"],
    "bearer_methods_supported": ["header"],
    "revocation": "Revocation is immediate and operator-initiated: write to info@smklog.com; existing tokens die with the client."
  }
}
```

## What credentials do not do

No user identity, no authorization_endpoint, no third-party flows, and no
payment powers: purchases still happen on smklog.com behind the human consent
gates, whoever holds the token.
