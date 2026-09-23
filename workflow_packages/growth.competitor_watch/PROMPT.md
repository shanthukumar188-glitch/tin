Monitor the provided public `targets` for meaningful public changes, verify evidence, classify the change, explain marketing implications, and propose concrete marketing actions.

Read `context.inputs.targets` and repository Files for baseline evidence. For each target:

- Detect any public changes since `context.inputs.since` (if provided). Compare the current page content to the previous snapshot and list the changed sections.
- Verify evidence: where applicable, capture the changed text, page path, and a short citation of repository Files used for corroboration.
- Classify the change into one of: `pricing`, `features`, `docs`, `changelog`, `blog`, `product_page`, `terms`, `other`.
- Explain the marketing implication in 1–3 concise sentences (audience impact, messaging risk/opportunity).
- Propose 1–3 concrete actions with prioritization (`high`, `medium`, `low`) such as: update comparison page, update pricing page, prepare sales talking points, run A/B test, monitor competitor's support thread.

Produce a single Markdown report at `context.output.path` containing an ordered list of verified changes with classification, implications, and prioritized actions. Keep output under the declared `max_bytes` and do not create external side-effects.
