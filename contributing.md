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

### Relevant issues

Use this section to reference any relevant issues or add other links to things this PR addresses.

For example:
> Closes BUG-123, relates to FEAT-456

### Summary

Use this section to explain why the changes in this PR have been done this way.

Though it's tempting to point to task tracking systems like Jira to explain why a change has been made, this section aims to answer the engineering side of the story, focusing on why we've chosen this implementation of the product solution described in our task tracking system issue.

Consider including [code snippets](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks) and/or [diagrams](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams) to provide visual explanation of concepts.

### Changes made

Use this section to concisely describe what the changes in this PR are.

The template includes bullet points here to help keep things brief and focused.
In smaller PRs, these bullet points might closely align with the commit messages, this is ok.

### Media

Use this section to show how the changes will affect the application.

This might take the form of before and after screenshots or videos. A video highlighting the changes made by this PR could also be acceptable.