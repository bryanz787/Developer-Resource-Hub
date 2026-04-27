# Developer AI Resource Hub

A growing, crowd-sourced compendium of AI tools, workflows,  and best practices for the development lifecycle.

## Quick start


| Goal                                | Where to look                      |
| ----------------------------------- | ---------------------------------- |
| Prompt / skill templates            | [templates/](templates/)           |
| Tool write-ups and links            | [tools/](tools/)                   |
| How to suggest content or open a PR | [CONTRIBUTING.md](CONTRIBUTING.md) |


## Repository layout

### [templates/](templates/)

Reusable structures for coding agents and editors.

- **[templates/CLAUDE.md](templates/CLAUDE.md)** — Starter outline for a global `~/.claude/CLAUDE.md` or a repo-specific Claude Code instructions file (project structure, commands, conventions, architecture notes).
- **[templates/skills/draft-pr-from-branch-diff.md](templates/skills/draft-pr-from-branch-diff.md)** — Skill-style guide to turn a git diff against a named base branch into a clear PR description, aligned with this repo’s [pull request template](.github/pull_request_template.md) when present.

### [tools/](tools/)

Short, structured notes on AI-related tools (category, link, rationale, cost, compatibility). Each file is a self-contained reference you can extend or mirror for new tools.

- **[tools/superpowers.md](tools/superpowers.md)** — [Superpowers](https://github.com/obra/superpowers): composable agent skills and methodology for planning, multi-agent work, reviews, and more.

### [.github/](.github/)

Automation and contributor-facing templates: **Suggest a Tool**, **Suggest a Template**, and the [pull request template](.github/pull_request_template.md) for PR descriptions.

## Contributing

We welcome contributions. See [CONTRIBUTING.md](CONTRIBUTING.md) for:

- Suggesting a tool (issue template: **Suggest a Tool**)
- Suggesting a template or skill (**Suggest a Template**)
- PR expectations and content guidelines

---

**Last updated:** 2026-04-27