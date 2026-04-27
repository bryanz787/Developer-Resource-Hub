---
name: draft-pr-from-branch-diff
description: Compares the current git branch to a user-named base branch and writes a pull request message. If `.github/pull_request_template.md` exists, follow that file’s structure; otherwise use a fixed plain-language template (Description, What I did, Notes, Usage). Use when the user names another branch and wants a PR description, merge request text, or changelog-style summary from the diff; also when they ask for a non-technical or concise PR write-up from branch differences.
---

# Draft PR from branch diff

## Goal

Turn the **git difference between the current branch and a named branch** into a **short, accurate PR message** that a non-technical reader can follow. Prefer clarity over jargon; omit implementation detail unless it changes behavior someone would notice.

## When the user names the base branch

Use the branch name they give (e.g. `main`, `development`, `origin/main`). If ambiguous (local vs remote), prefer `origin/<name>` when it exists after fetch.

## How to get the diff

1. **Current branch:** `git branch --show-current` (or `git rev-parse --abbrev-ref HEAD`).
2. **Ensure the base ref exists:** `git rev-parse --verify <base-branch>`; if it fails, `git fetch origin` and retry with `origin/<base>` if appropriate.
3. **What to diff (default for PRs):** three-dot form from base to HEAD — shows changes introduced on the current branch since it diverged from base:

   ```bash
   git diff <base-branch>...HEAD
   ```

   Use this unless the user explicitly wants **all** commits reachable from either side (then two-dot `..`).

4. **High-level context (optional but useful):** `git log <base-branch>..HEAD --oneline --no-decorate` for a commit list; `git diff <base-branch>...HEAD --stat` for file scope.

5. **Scope:** If the diff is huge, prioritize user-visible outcomes, config/env changes, breaking changes, and migration steps; still list major areas touched under **What I did**.

## Repository PR template (primary)

Before finalizing the PR body, look for `.github/pull_request_template.md` in the repo. If that file exists, read it and treat its section structure, headings, placeholders, and writing conventions as the **primary** source of truth. Summarize the diff into that template (filling or replacing placeholders as appropriate). If it does not exist, use the default output format below.

## Output format (default when no repo template)

If there is no `.github/pull_request_template.md`, use exactly these section headings and order:

```markdown
**Description:**

[Why this change exists and what problem it solves, in plain language. 1–3 short paragraphs max, bullet points can be used for concise, rapid-fire details.]

**What I did:**

- [Concrete outcome or area, not file names unless they matter to reviewers, format this in the style of 1 short paragraph followed by a list of bullet points breaking down changes by responsibility and impact, the use of indents should be employed to express hierarchy and relation]

**Notes:**

[Review focus: risk areas, how to test, follow-ups, or "none" if truly nothing. Keep brief.]

**Usage:**

[Only when new APIs, env vars, scripts, or contracts are introduced: minimal example or steps. Otherwise: "N/A" or omit the section body with a single line: **Usage:** N/A]
```

## Writing rules

- When the repository’s `.github/pull_request_template.md` is in use, prefer its implied rules over the default-format bullets that follow.
- **Description:** User or business framing first ("Users can…", "Fixes…", "Prepares for…"). Avoid stack dumps of technologies unless the PR is purely tooling.
- **What I did:** Bullet list; each line one idea; past tense; no paragraph blocks.
- **Notes:** Deployment, data migration, feature flags, auth, or "please verify on staging" — only what helps review or release.
- **Usage:** Real snippets or env examples; skip if nothing new for other developers to call or configure.
- Do **not** paste raw diff into the PR body. Summarize.
- If the diff is only docs/formatting, say so honestly in **Description** and keep **What I did** short.
- Deliver the final PR message in the form of a .MD file such that the user can keep the formatting consistent when pasting into github
- Do **not** overuse bold formatting
- If there is a specific file which a change can be largely or completely associated with, link the file as hypertext if the PR explicitly references a key change made to it

## Verification

- Re-read bullets against the diff: every significant change category should appear somewhere; nothing claimed that the diff does not support.
- If unsure whether a change was intentional, pask the user to clarify before proceeding, if no satisfactory answer provided, list under **Notes** as a question for reviewers.
