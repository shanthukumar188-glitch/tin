---
name: competitor-watch
description: Identify and prioritize competitor channels, sites and product pages to monitor for market signals.
---
 
Read repository Files for baseline evidence and `context.inputs.targets` for the list of public pages to watch. For each target, perform the following and return a JSON object (one per change) inside a Markdown code block:

- `target`: the URL or identifier watched
- `change_summary`: a short sentence describing the change
- `classification`: one of `pricing`,`features`,`docs`,`changelog`,`blog`,`product_page`,`terms`,`other`
- `evidence`: the changed text snippet(s) and the page path where found
- `comparison`: brief note of what changed compared to previous snapshot (if `context.inputs.since` provided)
- `implication`: 1–3 sentence marketing implication
- `actions`: an array of suggested actions, each with `{ "action": "...", "priority": "high|medium|low" }`
- `confidence`: `high` | `medium` | `low`

`evidence` must avoid private contact details and prefer public URLs, changelog excerpts, and cited repository File paths. When making claims that use repository Files for corroboration, include file paths.
