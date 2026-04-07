---
type: documentation
aliases:
  - AI Agents Guide
  - Gemini Codex Guide
description: Technical guide for non-Claude AI coding agents (Gemini CLI, Codex, Cursor, Windsurf). Simplified and portable version of CLAUDE.md. Reference when any AI agent other than Claude Code is operating in the CMDS vault.
author:
  - "[[구요한]]"
date created: 2026-01-02T16:30
date modified: 2026-04-07T21:15
tags:
  - CMDS
  - system
audience: Gemini CLI, Codex, Cursor, Windsurf
scope: technical-implementation
precedence: 2
memory-type: feedback
required-for:
  - code-generation
  - file-creation
  - file-editing
optional-for:
  - search
  - analysis
token-estimate: 3200
CMDS: "[[📚 501 Obsidian]]"
index: "[[🏛 CMDS Head Quarter]]"
version: "2.1"
status: completed
changelog:
  - "2.1 (2026-04-07): 필수 프로퍼티 7개로 확장 (description 추가, English required)"
  - "2.0 (2026-04-01): @include 기반 공통 규칙 분리, 중복 60% 제거"
  - "1.0 (2026-03-30): 초기 버전, frontmatter 표준 추가"
---
> **🔄 Last Updated: 2026-04-01** | Backup: `40. Docs/47. CMDS Docs/cmds-system-files/AGENTS_backup.md`

# AGENTS.md

This file provides guidance to AI coding agents (Gemini CLI, Codex, Cursor, Windsurf, etc.) when working with this Obsidian vault.

> **📌 Related System Files (5 Core Files)**
> - @CLAUDE.md → [[CLAUDE.md]] - Claude Code specific instructions (precedence: 1)
> - @AGENTS.md → [[AGENTS.md]] - This file (precedence: 2)
> - @CMDS.md → [[CMDS.md]] - System philosophy & user context (precedence: 3)
> - @🏛 CMDS Guide → [[🏛 CMDS Guide]] - Standards & templates (precedence: 4)
> - @🏛 CMDS Head Quarter → [[🏛 CMDS Head Quarter]] - Navigation hub (precedence: 5)

---

## Project Overview

This is an Obsidian vault for the **CMDSPACE (커맨드스페이스)** knowledge management system created by 구요한 (Yohan Koo). It implements the CMDS framework - a comprehensive Personal Knowledge Management (PKM) system with 9 major categories (100-900 series).

**Vault Scale**: 7,660+ notes, 120+ plugins, 90+ templates

### Working Environments & Sync
Two Macs are synced via **Obsidian Sync** (official Obsidian cloud server). All subfolders and files are kept identical.

| Environment | Machine | Base Path |
|-------------|---------|-----------|
| Primary | MacBook Pro (16-inch) | `/Users/yohankoo/Local Obsidian_MBP/CMDSPACE_Local_MBP` |
| Secondary | Mac Studio | `/Users/yohankoo/Obsidian_Local/CMDSPACE_Studio_Local_Org` |

---

<!-- STATIC: 아래 규칙은 거의 변경되지 않습니다 -->

## Critical Rules

> 공통 규칙은 `.claude/rules/` 에 정의되어 있습니다. 아래는 AI 에이전트가 반드시 따라야 할 핵심 규칙입니다.

@.claude/rules/indentation-rules.md

@.claude/rules/frontmatter-standard.md

@.claude/rules/wikilink-rules.md

@.claude/rules/file-creation-rules.md

---

## Essential (Post-Compact)

> 컨텍스트 압축 후에도 반드시 기억해야 할 핵심 규칙:
> 1. **YAML frontmatter: 2 SPACES** / **Markdown body: TAB**
> 2. **Wikilinks in YAML: 반드시 큰따옴표** `"[[link]]"`
> 3. **코드 출력 경로**: `00. Inbox/03. AI Agent/{환경 하위폴더}/`
> 4. **필수 프로퍼티 7개**: type, aliases, **description** (English, 1-2 sentences for LLMs), author, date created, date modified, tags
> 5. **날짜 포맷**: ISO 8601 (YYYY-MM-DD)

---

## Directory Structure & CMDS Categories

@.claude/rules/directory-structure.md

---

## Obsidian Wikilinks

```markdown
[[Note Name]]              # Basic link
[[Note Name|Display Text]] # Aliased link
[[Note Name#Heading]]      # Heading link
[[Note Name^block-id]]     # Block link
![[Note Name]]             # Embed file
![[image.png]]             # Embed image
```

---

<!-- DYNAMIC: 아래 내용은 주기적으로 갱신됩니다 -->

## Common Note Types

- `note` - General notes
- `terminology` - Term definitions
- `meeting` - Meeting minutes
- `people` - People profiles
- `curriculum` - Course curriculum
- `channel` - YouTube/Blog/Newsletter 채널 프로필
- `CMDS` - CMDS index pages (replaces traditional MOC concept)
- `documentation` - Technical docs

## Status Values

Standard status values (5 options):
- `unread` - Not yet processed
- `reading` - Currently reading
- `inProgress` - Work in progress
- `completed` - Finished
- `archived` - Historical reference

## File Prefixes

- 📎 - Web Clips
- 🏷 - Index pages
- 📦 - Reviews
- 🔖 - Personal outputs
- 📜 - Others' outputs
- 📈 - Code/Syntax
- 🎹 - Music
- 📘 - Books/Reference

## Templates

Templates are in `90. Settings/91. Templates/`. Key templates:

- `Template_00. Basic Note.md`
- `Template_01. Daily Note.md`
- `Template_05. Meeting Minutes.md`
- `Template_20. Research Note.md`
- `Template_51. People.md`

---

## Important Notes

1. **Use wikilinks `[[]]`** for internal references, NOT markdown links
2. **Respect existing patterns** - This is a mature vault with established conventions
3. **Check [[CMDS.md]]** for user context and workflow patterns
4. **Check [[🏛 CMDS Guide]]** for detailed standards and templates

---

**For Claude Code**: See [[CLAUDE.md]] for Claude-specific instructions.
**For LLM Context**: See [[CMDS.md]] for system philosophy and user profile.
