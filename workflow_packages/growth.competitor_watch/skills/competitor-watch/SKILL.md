---
name: competitor-watch
description: Identify and prioritize competitor channels, sites and product pages to monitor for market signals.
---

Read the project Files for context and the supplied `focus`. Use public signals (release notes, blog posts, product changelogs, author pages, and RSS feeds) to judge signal value. Prefer sources that:

n- regularly publish product or market updates
- have public changelogs, author pages, or RSS feeds
- cover features and positioning closely related to the project's `focus`

Produce a ranked shortlist with up to `context.inputs.max_results` entries. For each entry output a JSON object in a Markdown code block with keys: `name`, `type`, `justification`, `monitor_channel`, `monitor_hint`, `confidence`, `monitor_action`.

`confidence` is one of `high`, `medium`, `low`. `monitor_hint` should be a publicly discoverable URL pattern (feed URL, author page, changelog path) and must not include private or unverified contacts.

When using repository evidence (README, ABOUT, product pages), cite the file path(s) that supported your claim.
