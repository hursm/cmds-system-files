# CMDS System Files

> 5 Core System Files + 5 Shared Rules + 9 Architecture Patterns that power the CMDSPACE Personal Knowledge Management ecosystem.

## Live Demo

**https://system.cmdspace.work**

## Overview

CMDS (CMDSPACE) is a comprehensive Personal Knowledge Management (PKM) system built on Obsidian with 10,000+ notes. This repository contains the core system files that provide complete guidance for AI agents and human users working with the vault.

## What's New in v3.0

- **Shared Rules** (`.claude/rules/`): 5 common rule files shared via `@include` between CLAUDE.md and AGENTS.md, eliminating 60% duplication
- **9 Architecture Patterns**: precedence, STATIC/DYNAMIC markers, @include, Essential (Post-Compact), agent scoping, memory-type, token-estimate, changelog, shared rules
- **Changelog**: Version history tracking across all system files
- **Enhanced Frontmatter**: `precedence`, `memory-type`, `required-for`, `optional-for`, `token-estimate`, `changelog` fields

## Repository Structure

```
files/
├── CLAUDE.md              # Claude Code technical guide (precedence: 1)
├── AGENTS.md              # Other AI agents guide (precedence: 2)
├── CMDS.md                # System philosophy for all LLMs (precedence: 3)
├── CMDS-Guide.md          # Operational standards (precedence: 4)
├── CMDS-Head-Quarter.md   # Navigation hub (precedence: 5)
└── CMDS-System-Files.zip  # All files bundled

rules/
├── indentation-rules.md      # YAML 2-spaces / Markdown TAB
├── frontmatter-standard.md   # Required 6 properties + format
├── file-creation-rules.md    # Output path, naming, project folders
├── wikilink-rules.md         # Obsidian wikilink syntax + YAML quoting
└── directory-structure.md    # Vault folder structure + CMDS categories

CHANGELOG.md               # Version history
```

## The 5 Core Files

### For AI Agents (loaded into context window)

| File | Audience | Focus | Precedence |
|------|----------|-------|:----------:|
| **CLAUDE.md** | Claude Code | Technical implementation (HOW) | 1 |
| **AGENTS.md** | Gemini, Codex, Cursor | Portable technical rules (HOW) | 2 |
| **CMDS.md** | All LLM assistants | Context & philosophy (WHY/WHAT) | 3 |

### For Humans (referenced in Obsidian)

| File | Audience | Focus | Precedence |
|------|----------|-------|:----------:|
| **CMDS Guide** | User + AI | Operational standards | 4 |
| **CMDS Head Quarter** | User | Navigation hub | 5 |

## Architecture Patterns (from Claude Code Source Analysis)

| # | Pattern | Purpose |
|---|---------|---------|
| 1 | **precedence** | File priority ordering (1-5) for conflict resolution |
| 2 | **STATIC/DYNAMIC** | Cache-aware sections for AI processing |
| 3 | **@include** | Shared rules via file inclusion (AI reads inline) |
| 4 | **Essential** | Post-compact recovery — core rules that survive context compression |
| 5 | **required-for/optional-for** | Agent scoping — which tasks need which files |
| 6 | **memory-type** | Maps to Claude Code's memdir types (feedback/user/reference) |
| 7 | **token-estimate** | Token budget awareness for AI load prioritization |
| 8 | **changelog** | Inline version history in each file's frontmatter |
| 9 | **shared rules** | Common rules in `.claude/rules/` shared via @include |

## @include vs [[wikilink]]

| Syntax | Purpose | Used By |
|--------|---------|---------|
| `@path` | AI reads file content inline | AI agents (Claude Code, etc.) |
| `[[name]]` | Obsidian internal link for navigation | Obsidian graph view, backlinks |
| Both together | `@file → [[file]]` | When both AI loading and human navigation needed |

## CMDS Process

```
Connect → Merge → Develop → Share
```

| Stage | Categories | What Happens |
|-------|-----------|--------------|
| **Connect** | 100 Themes | Discover ideas, capture interests |
| **Merge** | 200 Literature | Integrate knowledge, build theory |
| **Develop** | 300-600 | Collect data, apply methods, use tools |
| **Share** | 700-800 | Create content, publish, teach, consult |

## Getting Started

1. **Download** all files from [system.cmdspace.work](https://system.cmdspace.work)
2. **Place** system files in the root of your Obsidian vault
3. **Place** rules in `.claude/rules/` directory
4. **Customize** placeholders (`{your-name}`, `{vault-path}`, etc.)
5. **Reference** CMDS.md in your AI conversations for context

## Stats

| Metric | Value |
|--------|-------|
| Core System Files | 5 |
| Shared Rules | 5 |
| Architecture Patterns | 9 |
| CMDS Categories | 9 (100-900) |
| Subcategories | 91 |
| Vault Notes | 10,000+ |

## Download

- [Download All (ZIP)](https://system.cmdspace.work/files/CMDS-System-Files.zip)
- [Browse Files](https://system.cmdspace.work/#download)

## Links

- [Profile](https://litt.ly/cmds)
- [YouTube](https://www.youtube.com/@cmdspace)
- [X (Twitter)](https://x.com/YohanKoo)
- [LinkedIn](https://www.linkedin.com/in/yohan-koo-a1baa3138/)
- [Threads](https://www.threads.com/@cmds_pace)
- [Education](https://class.cmdspace.kr/)

## License

All intellectual property rights belong to CMDSPACE.

---

Last Updated: 2026-04-01
