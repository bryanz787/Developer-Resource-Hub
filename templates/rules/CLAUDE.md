## Pre-amble
For tailored results for your codebase, claude code supports `/init` which analyzes your codebase to detect build systems, test frameworks, and code patterns, giving you a solid foundation to refine. This file provides a structure that you can use as a guide when ogranizing your global `CLAUDE.md` file (`~/.claude/CLAUDE.md`) or your repository specific file (`.claude/CLAUDE.d`)


# Project Title

Short project description and purpose

## Project Structure

Break down the organizational scheme of your project, if it includes multiple sub-repos (server, web, ios, android, etc) detail the tech stack and its distinction from other sub-repos

## Commands

Organize frequently used and important commands

## Conventions

Detail conventions you'd like Claude to follow while editing the codebase, below are some examples
- **Linting:** Run lint before committing.
- **Tests:** Run tests in the relevant package before committing.
- **Commits:** Use conventional commit prefixes (`fix:`, `feat:`, `refactor:`, `chore:`, etc.) while writing commit drafts, do not commit to github without explicit approval.
- **Versioning:** Repository follows SemVer convention in `file`.
- **Branch:** Main development branch is `placeholder`.

## Architecture Notes

Add details about the codebase that Claude frequently misses here.