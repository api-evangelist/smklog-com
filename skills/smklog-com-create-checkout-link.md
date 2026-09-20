---
name: create-checkout-link
description: Prepare a Stripe payment session for a chosen parcel rate; a human completes payment behind SMKlog consent gates.
---

# Create a checkout link for a parcel label

Turn a quoted rate into a payment session URL. The agent prepares the
session; a human opens the URL, confirms the shipping consents and pays.
The agent never charges anything.

## Call

First get a quote (see get-parcel-quote). Then
`POST https://quote-api.smklog.com/a2a` (JSON-RPC `message/send`) with a
DataPart naming the same shipment plus optional `"service"` to pick a
specific rate, or drive the MCP tool at `POST /mcp`. The reply carries the
live amount and a handoff URL on smklog.com.

The reply also carries `session_id`. Keep it: the MCP tool
`get_checkout_status` (or `GET /agent/checkout-session/<session_id>`) reports
whether the human has paid and whether the label exists, with the tracking
number once it does. Sessions live 30 days.

## Ground rules

Payment happens only on the human-confirmed page. Consents (contents
certification, carrier adjustment terms) are collected there, not from the
agent. Labels for restricted items are refused at quote time, not after
payment.
