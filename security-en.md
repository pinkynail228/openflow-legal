---
layout: page
title: OpenFlow Security
permalink: /security-en.html
---

## Report a vulnerability

Send a private message to [Telegram @pnklrd](https://t.me/pnklrd) marked
`OpenFlow security`. Do not publish working exploits, invite keys, provider keys,
document content, or personal data. Include the affected version/component, safe
reproduction steps, expected and actual results, and possible impact.

We aim to acknowledge reports within three business days, make an initial
assessment within 14 days, and communicate material status changes. There is no
public bug bounty at this time.

## Beta security model

- Mermaid authoring, Preview, Apply, and legend need no network request.
- Figma network access is restricted to one HTTPS relay domain.
- Relay fixes upstream/model and rejects client Authorization and upstream URLs.
- Provider key stays outside Figma as a server-side system credential.
- Invite keys are checked by SHA-256 hash and are revocable.
- Request size, rate, concurrency, and daily quota are bounded.
- Relay does not store or log prompt or response bodies.
- UI and main independently validate FlowSpec/placed payload and geometry before
  document mutation; updates use atomic group replacement.

OpenFlow beta claims no SOC 2, ISO 27001, or other independent certification.
