Produce a project-local outreach shortlist for bloggers, writers, podcasters and similar content creators who plausibly cover the project's focus.

Read the provided `focus` input and any short project context available in project Files. Search the public web (using only the model's knowledge and the repository evidence; do not call external APIs), identify up to `max_results` candidate authors, hosts or shows, and prioritize them by expected relevance and ease of contact.

For every selected candidate produce:
- name
- affiliation (site, publication, podcast)
- short justification (one sentence: why they're relevant)
- preferred contact channel and publicly discoverable contact handle or email pattern
- suggested one-sentence outreach opener tailored to that candidate and the project's `focus`

Produce the final output as a single Markdown file at `context.output.path`. Do not send messages, create PRs, or change files outside the declared artifact. Keep output under the declared `max_bytes`.

If public contact details are not discoverable with high confidence, provide an email-finding pattern (e.g. first.last@domain) and a note about confidence. Cite evidence paths from the project Files when you use them.

Do not invent private emails or phone numbers. When unsure, recommend how the founder can verify contact details safely.
