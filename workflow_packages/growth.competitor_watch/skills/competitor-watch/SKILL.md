---
---
name: competitor-watch
description: Identify and prioritize competitor channels, sites and product pages to monitor for market signals.
---

Read repository Files for baseline evidence and `context.inputs.competitor_urls` for the list of public pages to watch. For each competitor URL, return at most one JSON object (one per verified change) inside a Markdown code block with these keys:

- `url`: the competitor URL watched
- `change_summary`: a short sentence describing the observed change
- `classification`: one of `pricing`,`features`,`docs`,`changelog`,`blog`,`product_page`,`terms`,`other`
- `evidence`: the changed text snippet(s) and the public page path where found (or `unverified` if not corroborated)
- `comparison`: brief note of what changed compared to previous snapshot (if `context.inputs.since` provided)
- `implication`: 1–3 sentence marketing implication for the product team
- `actions`: an array of suggested actions, each with `{ "action": "...", "priority": "high|medium|low" }`
- `confidence`: `high` | `medium` | `low`

Guidelines:
- Only use public-source evidence. Do not attempt to access private resources or require authentication.
- When using repository Files for corroboration, include exact file path(s) used as evidence.
- Do not include private personal data or contact details in `evidence`.
- If a claim cannot be verified, mark `evidence` as `unverified` and set `confidence` to `low`.

Produce one combined Markdown report at the declared output path (`reports/COMPETITOR_WATCH.md`) that contains an ordered list of verified changes (as JSON blocks), a short executive summary, and a prioritized action queue (max 5 actions). Keep output concise and under the declared `max_bytes`.

Safety:
- This skill performs public-source analysis only. Do not attempt to bypass access controls, contact people, or alter external sites.
