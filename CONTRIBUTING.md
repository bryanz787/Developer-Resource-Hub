# Contributing to Developer AI Resource Hub

This document describes how we expect people to participate, based on the repository’s GitHub automation and templates under [.github/](.github/).

## Ways to contribute

Aligned with [README.md](README.md), typical contributions include:

- Suggesting a tool (use the issue template below).
- Adding or refining workflows, skills, prompts, or documentation.
- Fixing factual errors or broken links.
- Sharing concise case studies or usage notes where they fit the repo structure.

## Issues

### Tool suggestions

For **new AI tool recommendations**, open an issue and choose **“Suggest a Tool”**. That template (see [.github/ISSUE_TEMPLATE/suggest_tool.md](.github/ISSUE_TEMPLATE/suggest_tool.md)) expects:

| Section | What to include |
|--------|------------------|
| **Title** | Prefix with `[TOOL] ` (the template sets this pattern). |
| **Tool name** | Exact product or project name. |
| **Category** | One of: Text Generation, Code Generation, Testing/Debugging, Documentation, Code Review, or Other (specify). |
| **Link** | Canonical URL (homepage, docs, or official listing). |
| **Why recommend it** | 2–3 sentences on the developer problem it solves. |
| **Cost** | Free, free tier + paid, subscription (note approximate cost if known), or Enterprise. |
| **Your experience** | Whether you have used it and for how long. |
| **Comparison** | How it relates to tools already covered in this hub (overlap, differentiation, or gap). |

The template applies the label **`tool-suggestion`** when used via GitHub’s issue chooser.

### Other changes

For corrections, new sections, or non-tool work, open a **blank issue** or a future dedicated template if one is added. Describe the change, link to affected files, and note whether you are willing to open a PR.

## Pull requests

PRs should follow the structure implied by [.github/pull_request_template.md](.github/pull_request_template.md):

1. **Description** — Rationale and context for the change (why, not only what).
2. **What I did** — Bullet list of concrete edits (files, sections, or behaviors).
3. **Notes** — Anything reviewers should watch for (tradeoffs, open questions, follow-ups).
4. **Usage** — If you introduce something another contributor must consume (APIs, scripts, folder conventions), add minimal examples or pointers.

Keep changes scoped: prefer focused PRs over large mixed-topic diffs unless maintainers agree otherwise.

## Content and tone

- Prefer **accurate, verifiable** links and names; avoid hype or unsubstantiated claims.
- Match **existing folder layout and naming** in the repo unless an issue/PR explicitly proposes a new convention.
- For lists and templates, stay **consistent with nearby files** (tone, heading style, checklist format).

## Licensing and conduct

If the repository adds a `LICENSE` or community guidelines file, follow those documents for legal terms and behavior expectations. Until then, assume good faith, respect reviewer time, and keep discussion technical and constructive.

## Summary checklist

- [ ] Tool idea? Use **Suggest a Tool** and fill every section.
- [ ] PR? Fill **Description**, **What I did**, **Notes**, and **Usage** (when relevant).
- [ ] Link README or index files if you add new top-level resources.

Questions are welcome via issues before large refactors.
