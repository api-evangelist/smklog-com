# SMKlog

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SMKlog (SMKLOG-2022 LLC, Berkeley Heights, New Jersey) is an independent US parcel shipping calculator and label seller: describe an item in plain words, get live USPS, UPS, FedEx and DHL Express rates from a US origin to the US, Canada, the UK, Germany or Australia, and buy the label online. The same pricing engine is published for machines as the SMKlog Quote API on quote-api.smklog.com: an OpenAPI 3.1 contract with no key required, a remote MCP server with five tools (plus an open-source stdio bridge), an A2A agent card, an RFC 9727 api-catalog, RFC 8414/9728 OAuth metadata for an optional client_credentials rate-limit tier, two provider-published Agent Skills and an llms.txt. Agents price and prepare checkout; a human always completes payment on smklog.com.

**Areas:** Company · Shipping · Logistics · Parcel Shipping · shipping-rates · Shipping Labels · E-Commerce · Agents · MCP · A2A

## SMKlog on APIs.io

Everything profiled for SMKlog is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/smklog-com/](https://apis.io/providers/smklog-com/)** — or go straight to one of the APIs or properties below.

### APIs (3)

- [SMKlog Checkout API](https://apis.io/apis/smklog-com/smklog-com-checkout-api/) — Agent-prepared payment sessions completed by a human on smklog.com.
- [SMKlog Operations API](https://apis.io/apis/smklog-com/smklog-com-operations-api/) — Liveness.
- [SMKlog Quotes API](https://apis.io/apis/smklog-com/smklog-com-quotes-api/) — Live parcel rate quotes from a US origin.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [SMKlog Parcel Shipping Rates](https://apis.io/servers/smklog-com/smklog-quotes/)

#### JSON Schema (9)

The data models the API reads and writes.

- [CheckoutSession](https://apis.io/schemas/smklog-com/smklog-com-checkout-session/)
- [CheckoutSessionRequest](https://apis.io/schemas/smklog-com/smklog-com-checkout-session-request/)
- [CheckoutStatus](https://apis.io/schemas/smklog-com/smklog-com-checkout-status/)
- [Liveness](https://apis.io/schemas/smklog-com/smklog-com-liveness/)
- [Package](https://apis.io/schemas/smklog-com/smklog-com-package/)
- [Problem](https://apis.io/schemas/smklog-com/smklog-com-problem/)
- [QuoteRequest](https://apis.io/schemas/smklog-com/smklog-com-quote-request/)
- [QuoteResponse](https://apis.io/schemas/smklog-com/smklog-com-quote-response/)
- [Rate](https://apis.io/schemas/smklog-com/smklog-com-rate/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Smklog Com Context](https://apis.io/jsonld/smklog-com/smklog-com-context/)

#### Examples (6)

Example requests and responses.

- [Smklog Com Create Payment Session Request Example](https://apis.io/examples/smklog-com/smklog-com-create-payment-session-request-example/)
- [Smklog Com Create Payment Session Responses Example](https://apis.io/examples/smklog-com/smklog-com-create-payment-session-responses-example/)
- [Smklog Com Get Checkout Status Responses Example](https://apis.io/examples/smklog-com/smklog-com-get-checkout-status-responses-example/)
- [Smklog Com Get Parcel Quote Request Example](https://apis.io/examples/smklog-com/smklog-com-get-parcel-quote-request-example/)
- [Smklog Com Get Parcel Quote Responses Example](https://apis.io/examples/smklog-com/smklog-com-get-parcel-quote-responses-example/)
- [Smklog Com Status Responses Example](https://apis.io/examples/smklog-com/smklog-com-status-responses-example/)

#### Collections (1)

Postman and Open Collection request collections.

- [SMKlog Quote API 1.4.0](https://apis.io/collections/smklog-com/postman-smklog-com-quote-api/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Smklog Com Agent Crosswalk Overlay](https://apis.io/overlays/smklog-com/smklog-com-agent-crosswalk-overlay/)
- [Smklog Com Quote Api Overlay](https://apis.io/overlays/smklog-com/smklog-com-quote-api-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [SMKlog API Rules](https://apis.io/rules/smklog-com/smklog-com-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Smklog Com Authentication](https://apis.io/security/smklog-com/smklog-com-authentication/)
- [Smklog Com Domain Security](https://apis.io/security/smklog-com/smklog-com-domain-security/)
- [Smklog Com Vulnerability Disclosure](https://apis.io/security/smklog-com/smklog-com-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Smklog Com Scopes](https://apis.io/scopes/smklog-com/smklog-com-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Smklog Com Plans Pricing](https://apis.io/plans/smklog-com/smklog-com-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Smklog Com Rate Limits](https://apis.io/rate-limits/smklog-com/smklog-com-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Smklog Com Finops](https://apis.io/finops/smklog-com/smklog-com-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://smklog.com/)
- [Documentation](https://smklog.com/api)
- [Getting started](https://smklog.com/repack-line)
- [API reference](https://quote-api.smklog.com/openapi.json)
- [Pricing](https://smklog.com/pricing)
- [Support](https://smklog.com/support)
- [Changelog](https://smklog.com/news/)
- [Blog](https://smklog.com/lp/)
- [Security](https://smklog.com/.well-known/security.txt)
- [Compliance](https://smklog.com/trust/compliance)
- [Trust centre](https://smklog.com/trust/)
- [Terms of service](https://smklog.com/terms)
- [Privacy policy](https://smklog.com/privacy)
- [GitHub](https://github.com/smklog)
- [Status](https://smklog.com/developers/status)

## API Evangelist rating

**Kin Score 94.0** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 95.0 |
| Contract quality | 65.1 |
| Contract governance | 100.0 |
| Operational transparency | 92.1 |
| Developer ergonomics | 100.0 |
| Access clarity | 78.9 |

**Agent readiness 55.1** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | yes |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 76.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/smklog-com/](https://apis.io/providers/smklog-com/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for SMKlog: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/smklog-com/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
