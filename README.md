# Changelog Generator Skill

A Claude Code skill + bash script that generates a structured `CHANGELOG.md` from git history. Built for the [claude-builders-bounty $50 bounty](https://github.com/claude-builders-bounty/claude-builders-bounty/issues/1).

## Setup (3 steps)

1. Copy `scripts/changelog.sh` and `skills/generate-changelog/` into your project.
2. Make it executable: `chmod +x scripts/changelog.sh`
3. Run it: `bash scripts/changelog.sh` — or `/generate-changelog` in Claude Code.

## What it does

- Collects commits since the last git tag (full history if there are no tags; merge commits skipped)
- Auto-categorizes into `Added` / `Fixed` / `Changed` / `Removed` via conventional-commit prefixes + keyword heuristics
- Writes a Keep-a-Changelog style `CHANGELOG.md` with one bullet per commit

See [sample/CHANGELOG.md](./sample/CHANGELOG.md) for output generated from a real repo.

## Claim the bounty

1. Comment `/opire try` on [issue #1](https://github.com/claude-builders-bounty/claude-builders-bounty/issues/1)
2. Submit a PR with these files — payment releases automatically on merge
