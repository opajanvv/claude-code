# Claude Code setup

My personal configuration for [Claude Code](https://github.com/anthropics/claude-code), Anthropic's CLI tool for working with Claude.

This repo contains what I learned while using Claude Code for development. The structure is improving significantly after reading Teresa Torres's work on effective use of Claude Code at [producttalk.org](https://www.producttalk.org/).
That's why I decided to store in a Github repo: for my own reference, and for others to get ideas.

## Contents

- `CLAUDE.md` - Global instructions (symlinked to `~/.claude/CLAUDE.md`)
- `.claude/CLAUDE.md` - Project-specific instructions for this repo
- `commands/` - Custom slash commands
  - `plan.md` - Plan before implementing any feature or change
  - `review.md` - Direct feedback on texts and documents
  - `git-commit.md` - Quick commits with concise messages
  - `cleanup-downloads.md` - Remove old files from Downloads

## Setup

Symlink or copy files to `~/.claude/`:

```bash
ln -s $(pwd)/CLAUDE.md ~/.claude/CLAUDE.md
ln -s $(pwd)/commands/*.md ~/.claude/commands/
```
