# Claude Code setup

My personal configuration for [Claude Code](https://github.com/anthropics/claude-code), Anthropic's CLI tool for working with Claude. This repo is a work in progress.

This started as notes from my own experience using Claude Code for development. The structure is improving after reading Teresa Torres's posts on effective use of Claude Code at [producttalk.org](https://www.producttalk.org/). I decided to store it in a Github repo for my own reference and for others to get ideas.

## What is CLAUDE.md?

CLAUDE.md files give Claude persistent memory across conversations. See Teresa Torres's article [Give Claude Code a Memory](https://www.producttalk.org/give-claude-code-a-memory/) for the full explanation of the three-layer system.

## Contents

- `CLAUDE.md` - Global instructions (symlinked to `~/.claude/CLAUDE.md`)
- `.claude/CLAUDE.md` - Project-specific instructions for this repo
- `commands/` - Custom slash commands
  - `cleanup-downloads.md` - Cleanup Downloads
  - `commit-and-push.md` - Commit and push
  - `plan.md` - Plan
  - `review-text.md` - Review text
## Setup

Symlink or copy files to `~/.claude/`:

```bash
mkdir -p ~/.claude/commands
ln -s $(pwd)/CLAUDE.md ~/.claude/CLAUDE.md
ln -s $(pwd)/commands/*.md ~/.claude/commands/
```
