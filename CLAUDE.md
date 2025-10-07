# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Claude Code user configuration directory (`~/.claude`) storing settings, conversation history, and custom agents.

## What's Tracked in Git

- `agents/` - Custom agent definitions
- `settings.json` - User settings
- `.gitignore` - Repository configuration

Everything else (databases, history, plugins, projects) is runtime data.

## Custom Agents

Agent definitions in `agents/*.md` use frontmatter:

```yaml
---
name: agent-name
description: When and how to use this agent (include examples)
tools: Bash, Read
model: sonnet
color: yellow
---
```

**committer agent** - Uses gitmoji conventions, formats files before committing (.nix with nixfmt, .lua with stylua)

## Files

- `__store.db` - SQLite conversation history
- `history.jsonl` - JSONL conversation log
- `settings.json` - User settings (tracked)
- `settings.local.json` - Local settings (not tracked)
