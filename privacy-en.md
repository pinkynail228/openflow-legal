---
layout: page
title: OpenFlow Privacy Policy
permalink: /privacy-en.html
---

Effective date: July 14, 2026.

## Summary

Mermaid authoring, Preview, Apply, the built-in guide, and legend work locally and
do not send source over the network. OpenFlow has no accounts, analytics, ads, or
tracking SDKs. Do not submit secrets or sensitive personal, payment, medical, or
confidential information.

## Optional API processing

Only when a user chooses API generation, OpenFlow sends through
`https://openflow.baboonshop.ru`:

- the user's request;
- bounded OpenFlow API history;
- the current FlowSpec of an explicitly selected managed OpenFlow group;
- a revocable invite key used to authorize the relay.

OpenFlow does not read or send arbitrary Figma canvas content or selection.

## Storage

- Invite key: Figma `clientStorage` on the user's device only.
- Locale: a separate non-secret `clientStorage` preference.
- After explicit Apply: FlowSpec, bounded API history, origin, and non-secret
  metadata in private plugin data on the managed group.
- Unapplied draft: memory only and not restored after closing the plugin.
- Relay: SHA-256 invite-key hashes/status and 30-day daily usage aggregates only.
- Relay does not store or log prompts, chat, request/response bodies, provider
  responses, Authorization headers, upstream credentials, or user IP addresses.

## Third-party processing

Optional API requests are sent over HTTPS through the OpenFlow relay to OpenCode
Go using fixed model `deepseek-v4-flash`. See OpenCode's
[Privacy Policy](https://opencode.ai/legal/privacy-policy) and
[Terms](https://opencode.ai/legal/terms-of-service). The provider credential is a
server-side system credential and is never sent to Figma.

Users can remove the key in API, delete an OpenFlow group, or remove its data in
Figma. The beta author can revoke invite keys. Daily aggregates expire after 30 days.

Questions: [Telegram @pnklrd](https://t.me/pnklrd).
