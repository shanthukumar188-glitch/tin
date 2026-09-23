Produce a project-local competitor-monitoring shortlist.

Read the provided `focus` input and any short project context available in project Files. Treat `focus` as the competitive signal to monitor (a competitor domain, product page, or short explanation). Using only the model's knowledge and repository evidence (do not call external APIs), identify up to `max_results` competitor sites, authors, podcasts, or channels worth monitoring, and prioritize them by expected signal value and ease of monitoring.

For every selected candidate produce:
- name
- type (site, author, podcast, product page)
- short justification (one sentence: what signal they produce and why it's relevant)
- preferred channel to monitor (e.g., website, RSS, Twitter) and a publicly discoverable handle or feed URL pattern
- suggested monitoring action (e.g., "follow RSS", "watch product changelog", "add to social listening"), and an optional quick search phrase that would find relevant posts

Produce the final output as a single Markdown file at `context.output.path`. Do not send messages, create PRs, or change files outside the declared artifact. Keep output under the declared `max_bytes`.

If contact details are not relevant, prefer feed URLs, author page patterns, and public changelog locations. Cite repository File paths when you use project Files as evidence.

If the provided `focus` is ambiguous or missing, describe what's required (e.g., competitor domain, product page, or specific signal type) and suggest minimal clarifying inputs.
