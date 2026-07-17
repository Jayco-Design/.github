# Pull Requests

## General Guidance

If you're a PR reviewer, use this list to ensure you're thoroughly reviewing the PR.

If you're the PR author, use this list as self-review as the reviewer will be using the same criteria to assess the PR.

- Does the code in this PR follow good design patterns and avoid bad design patterns?
  - Is logic primarily in the service layer?
  - Does it avoid use of known bad patterns?
    - `SELECT *` queries
    - N+1 queries
- Do the commit messages describe the changes in each commit?
- Has the code been appropriately tested?
  - Have manual tests been done and recorded against the PR? If not, why not?
  - Have automated tests been added or updated accordingly?
- Has the documentation of this code been updated?
- Will these changes be deployed behind a feature flag? If not, why not?
- Have we intentionally not followed best practice anywhere? If so, has it been explained why?
- Have relevant labels been applied to the PR?
- Could this PR be reviewed by someone outside of this team? It's good for knowledge sharing

## Template Sections

Write the PR the way you'd explain it to a teammate: intent first, in plain English — *then* the details. Scale the detail to the change; never pad a small PR or flatten a big one.

### Author context

**Required, and written by you — not AI-generated.** Every PR opens with a brief explanation in your own words, above the rest of the description, covering:

- the **business context** behind the change, and
- any **trade-offs** you made, and why.

Everything below the divider may be AI-drafted; this block may not. A PR without it is incomplete. This is the PR's plain-English intent — there is no separate Summary section, so the description proper starts at *What changed*.

Consider including [code snippets](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks) and/or [diagrams](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams) to explain concepts visually.

### What changed

Concisely describe the changes, as bullets — one plain statement each. Describe the *behaviour*, not the file list. In smaller PRs these might align closely with the commit messages; that's fine. Where a change is complex or its reason isn't obvious, a bullet can carry a short *why* — the Author context covers the overall intent, so keep these to the per-change rationale.

Cut anything that doesn't earn its place:

- **File-by-file narration** — describe behaviour, not the component inventory.
- **Provenance** ("verified against X", "matches the legacy app") — that belongs in the commits.
- **Diff-restating** — if a bullet only says what the code obviously does, drop it.
- **Ceremony sections** — no Testing/Review boilerplate on a PR that doesn't need it.

### Relevant issues

Reference any relevant issues or link to what this PR addresses.

For example:
> Closes BUG-123, relates to FEAT-456

### Media

Show how the changes affect the application — before/after screenshots, or a short video highlighting the change. Worth it for anything with a UI.