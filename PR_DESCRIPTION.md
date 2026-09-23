Title: Add `growth.blogger_outreach` procedure workflow package

What this workflow does and who would run it
- Adds a Codex procedure package `growth.blogger_outreach` that builds a ranked
  outreach shortlist of bloggers, writers, podcasters and related creators tailored
  to a project's `focus`. Intended users: founders and small-product operators who
  want an actionable list of media contacts and one-line openers to run outreach.

Why it's missing today
- The repo includes analytics, product briefs and outreach examples (email
  campaign), but it lacks a lightweight, discovery-first shortlist workflow that
  targets creators and publishers rather than audience keywords or campaign
  setup. This fills that gap with a safe, read-only, project-local procedure.

How it works (implementation summary)
- Procedure package at `tin/workflow_packages/growth.blogger_outreach/` with:
  - `workflow.json` manifest declaring inputs and a single Markdown artifact output.
  - `PROMPT.md` that bounds behavior and output format.
  - `skills/growth-blogger-outreach/SKILL.md` describing candidate selection and
    output JSON structure.
- Executor: `codex.procedure` (isolated, fenced sandbox, 900s timeout). On run,
  the entry skill reads `focus` and project Files, then produces `reports/outreach/blogger_shortlist/{run_id}.md`.

Where the idea came from
- Inspired by common founder workflows (targeted blogger outreach, podcast
  guesting), and by examples in the repo that provide analytics and shortlist
  workflows. The approach emphasizes evidence citation and non-inventive
  contact hints.

Tests and validation
- This contribution is a source-only procedure package (no runtime tests added).
- Package follows `workflow_packages/README.md` manifest shape and example style.
- CI in the upstream repo will run `uv run tin-lite validate-community` on the PR.

Notes / things I couldn't fully automate
- I pushed the branch to your fork `feature/growth-blogger-outreach` but I could
  not create the cross-repository pull request to `github.com/tin-computer/tin`
  because GitHub authentication is required. Steps to open the PR are below.

Open PR steps (pick one):

1) Browser (quick):
   - Visit: https://github.com/shanthukumar188-glitch/tin/pull/new/feature/growth-blogger-outreach
   - Change the base repository to `tin-computer/tin` and the base branch (usually `main`).
   - Paste this file's content as the PR body and create the PR.

2) GitHub CLI (if authenticated):
   ```bash
   gh pr create --base tin-computer:main --head shanthukumar188-glitch:feature/growth-blogger-outreach \
     --title "Add growth.blogger_outreach procedure workflow package" \
     --body-file PR_DESCRIPTION.md
   ```

If you'd like, I can attempt to open the PR for you now if you authenticate `gh` locally, or provide a personal access token (not recommended in chat). Otherwise confirm and I'll mark the assignment complete and summarize changes for your submission.
