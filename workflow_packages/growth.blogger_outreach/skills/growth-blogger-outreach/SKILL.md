---
name: growth-blogger-outreach
description: Identify and prioritize relevant bloggers, writers and podcasters for outreach, and craft personalized one-line openers.
---

Read the project Files for context and the supplied `focus`. Use public signals (titles, recent posts, episode descriptions, topical keywords) to judge relevance. Prefer creators who:

- recently published on the topic (within ~12 months)
- demonstrate practical audience fit (their readers/listeners match the product's buyers)
- show contactability (email patterns, contact pages, producer PR emails, or active social handles)

Produce a ranked shortlist with up to `context.inputs.max_results` entries. For each entry output a JSON object in Markdown code block with keys: `name`, `affiliation`, `justification`, `contact_channel`, `contact_hint`, `confidence`, `one_liner`.

Confidence is one of `high`, `medium`, `low`. `contact_hint` must never be a fabricated personal email; prefer published emails or a domain-based pattern and note how to verify.

When using repository evidence (README, ABOUT, product pages), cite the file path(s) that supported your claim. If the `domains` input is provided, prefer candidates associated with those domains and note the tie.

If the prompt lacks sufficient focus or context to build even a short five-entry list, explain what's missing and suggest minimal inputs the founder can supply.
