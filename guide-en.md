---
layout: page
title: How to use OpenFlow
permalink: /guide-en.html
---

[Русская инструкция](guide.html)

# How to use OpenFlow

OpenFlow is a free Mermaid-first Community beta for Figma Design. Its primary
workflow is local and requires no registration, invite key, or network request.

## Mermaid: primary workflow

1. Open OpenFlow. **Mermaid** is selected by default.
2. Paste supported Mermaid source or select **Insert example**.
3. Select **Preview** and review nodes, transitions, and warnings.
4. Select **Add to Figma**. The canvas is unchanged before this explicit action.
5. To update a flow, select its managed group, reopen OpenFlow, edit Mermaid, and
   apply the changes.

Edited source must be validated again. While it is dirty, Apply and AI requests
are blocked so a stale FlowSpec cannot be used.

## API: optional AI beta

Open **API**, paste a revocable OpenFlow invite key, and select **Verify key**.
This is not a personal provider key; the OpenCode credential remains on the relay.
An accepted key is stored only in Figma `clientStorage` on that device.

After generation OpenFlow returns to Mermaid automatically. Review the source and
Preview, then explicitly apply the flow. API supports up to 15 nodes and 30
transitions; Mermaid/document supports up to 80/160. Any Community user may request
a free personal key through [Telegram @pnklrd](https://t.me/pnklrd).

## Kinds, branches, and errors

The built-in `?` guide explains all eight kinds and stable IDs. Only `decision`
and `decisionUser` may have 2–3 labeled outcomes. `end` and `error` are terminal.
A recoverable error is `card`/`subtle`; a later user choice is a separate
`decisionUser`. **Insert legend into Figma** creates ordinary editable content
without managed-flow markers.

The selected-flow menu contains **Reset manual positions** and **Clear API
history**. The interface and new AI output support RU/EN. Switching language does
not translate existing diagram labels or chat.

Do not send secrets or sensitive personal data. See the [Privacy Policy](privacy-en.html)
and [Beta Terms](terms-en.html). Send errors without an invite key to
[Telegram @pnklrd](https://t.me/pnklrd).
