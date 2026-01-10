# Claude Code setup

My personal configuration for [Claude Code](https://github.com/anthropics/claude-code), Anthropic's CLI tool for working with Claude.

This repo contains what I learned while using Claude Code for development. The structure improved significantly after reading Teresa Torres's work on effective collaboration and communication at [producttalk.org](https://www.producttalk.org/).

## Contents

- `CLAUDE.md` - Global instructions (symlinked to `~/.claude/CLAUDE.md`)
- `.claude/CLAUDE.md` - Project-specific instructions for this repo
- `commands/` - Custom slash commands
  - `review.md` - Direct feedback on texts and documents
  - `git-commit.md` - Quick commits with concise messages
  - `assess-file.md` - Analyze files and recommend keep/remove
  - `cleanup-downloads.md` - Remove old files from Downloads

## Setup

Symlink or copy files to `~/.claude/`:

```bash
ln -s $(pwd)/CLAUDE.md ~/.claude/CLAUDE.md
ln -s $(pwd)/commands/*.md ~/.claude/commands/
```
