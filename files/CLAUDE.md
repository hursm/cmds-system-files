---
type: documentation
aliases:
  - Claude Code Guide
  - CC System File
description: Claude Code 전용 기술 구현 가이드. 파일 생성/편집 규칙, YAML/MD 인덴트 규칙, 볼트 명령어, 코드 출력 경로를 정의한다.
author:
  - "[[{your-name}]]"
date created: 2025-09-27T17:53
date modified: 2026-04-01T11:30
tags:
  - CMDS
  - system
audience: Claude Code
scope: technical-implementation
precedence: 1
memory-type: feedback
required-for:
  - code-generation
  - file-creation
  - file-editing
optional-for:
  - search
  - analysis
  - reading
token-estimate: 5800
CMDS: "[[📚 501 Obsidian]]"
index: "[[🏛 CMDS Head Quarter]]"
version: "3.0"
status: completed
changelog:
  - "3.0 (2026-04-01): @include 기반 공통 규칙 분리, 9개 아키텍처 패턴 적용"
  - "2.1 (2026-03-30): frontmatter 표준 추가, 백업 경로 이동"
  - "2.0 (2026-03-15): 전면 리뷰, 통계 갱신, GitHub/Web 링크"
---
> **🔄 Last Updated: 2026-04-01** | Backup: `40. Docs/47. CMDS Docs/cmds-system-files/CLAUDE_backup.md` | GitHub: [cmds-system-files](https://github.com/{gpt-session-id}/cmds-system-files) | Web: [system.cmdspace.work](https://system.cmdspace.work)

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **📌 Related System Files (5 Core Files)** — `precedence` 순서대로 로드
> - @CLAUDE.md → [[CLAUDE.md]] - Technical implementation (precedence: 1)
> - @AGENTS.md → [[AGENTS.md]] - Other AI agents guide (precedence: 2)
> - @CMDS.md → [[CMDS.md]] - System philosophy & context (precedence: 3)
> - @🏛 CMDS Guide → [[🏛 CMDS Guide]] - Standards & templates (precedence: 4)
> - @🏛 CMDS Head Quarter → [[🏛 CMDS Head Quarter]] - Navigation hub (precedence: 5)

<!-- STATIC: 아래 내용은 거의 변경되지 않는 규칙입니다. AI는 높은 신뢰도로 캐시할 수 있습니다. -->

## ⚠️ CRITICAL RULES — READ FIRST

> 공통 규칙은 `.claude/rules/` 에 분리되어 있습니다. 아래는 핵심 요약입니다.

@.claude/rules/indentation-rules.md

@.claude/rules/frontmatter-standard.md

@.claude/rules/wikilink-rules.md

### Pre-Flight Checklist (Before Every Write/Edit)

Every time you create or edit a .md file, verify:

- [ ] **YAML frontmatter uses 2 SPACES** (not tabs)
- [ ] **Markdown body uses TAB** (not spaces)
- [ ] **Wikilinks in YAML are quoted**: `"[[link]]"` not `[[link]]`
- [ ] **Arrays use proper format**: hyphen + space + value
- [ ] **Dates use ISO 8601**: `YYYY-MM-DD` format
- [ ] **File saved in correct location**: Code → `00. Inbox/03. AI Agent/{environment subfolder}/`
- [ ] **Filename follows convention**: `YYYY-MM-DD-description.ext`

---

## Essential (Post-Compact)

> 컨텍스트 압축 후에도 반드시 기억해야 할 핵심 규칙:
> 1. **YAML frontmatter: 2 SPACES** / **Markdown body: TAB**
> 2. **Wikilinks in YAML: 반드시 큰따옴표** `"[[link]]"`
> 3. **코드 출력 경로**: `00. Inbox/03. AI Agent/{환경 하위폴더}/`
> 4. **필수 프로퍼티 6개**: type, aliases, author, date created, date modified, tags
> 5. **날짜 포맷**: ISO 8601 (YYYY-MM-DD)
> 6. **배열 포맷**: hyphen + space (`- value`)

---

## Project Overview

This is an Obsidian vault for the CMDSPACE knowledge management system created by {Your Name}. It implements the CMDS framework - a comprehensive Personal Knowledge Management (PKM) system with 9 major categories (100-900 series) and follows the CMDS Process: Connect → Merge → Develop → Share.

## 💻 Working Environments

This vault is accessed from two different Mac environments:

### Primary Environment (MacBook Pro) ✅
**Base Path**: `{vault-path}`

**System**: MacBook Pro (16-inch)
**Status**: Primary (Most Frequently Used)
**Usage**: Main development and knowledge management workstation

### Secondary Environment (Mac Studio)
**Base Path**: `{vault-path-studio}`

**System**: Mac Studio
**Status**: Secondary
**Usage**: Desktop workstation for heavy processing tasks

### Vault Sync
- Two machines are synced via **Obsidian Sync** (official Obsidian cloud server)
- The vault structure and all files/subfolders remain identical across both environments
- Sync is automatic and continuous — changes on one machine propagate to the other

### Important Notes:
- All relative paths in this document (e.g., `00. Inbox/03. AI Agent/`) are relative to the base path above
- When switching between environments, Claude Code will automatically use the appropriate base path
- AI coding outputs are separated by environment subfolder (`03-1` ~ `03-4`) to track which machine/agent created each file

---

## System Documentation Structure

This vault has **5 core system files** that work together to provide complete guidance:

### 🤖 AI Documents (loaded into context window)

| File                      | Purpose                        | Audience              | Focus                                               |
| ------------------------- | ------------------------------ | --------------------- | --------------------------------------------------- |
| **CLAUDE.md** (this file) | Technical implementation guide | Claude Code           | **HOW** - Code workflows, file operations, commands |
| **AGENTS.md**             | General AI coding agent guide  | Gemini CLI, Codex etc | **HOW** - Technical rules for other AI agents       |
| **CMDS.md**               | Context & philosophy guide     | All LLM assistants    | **WHY & WHAT** - System purpose, user context       |

### 👤 Human Documents (referenced in Obsidian)

| File                        | Purpose               | Audience  | Focus                                 |
| --------------------------- | --------------------- | --------- | ------------------------------------- |
| **🏛 CMDS Head Quarter.md** | Navigation hub        | User      | **WHERE** - Category map, quick links |
| **🏛 CMDS Guide.md**        | Operational standards | User + AI | **STANDARDS** - Properties, templates |

### When to Use Which File

- **You are here (CLAUDE.md)**: For Claude Code technical implementation
	- File creation/editing rules
	- Obsidian-specific syntax (wikilinks, YAML)
	- Vault commands and operations
	- Code output location (`00. Inbox/03. AI Agent/`)

- **Use AGENTS.md**: For other AI coding agents (Gemini CLI, Codex, Cursor, etc.)
	- General technical rules without Claude-specific content
	- Simpler, more portable structure

- **Use CMDS.md**: For understanding context and purpose
	- Why this system exists
	- User's professional background and workflow
	- Detailed explanation of 9 categories (100-900)
	- CMDS Process (Connect → Merge → Develop → Share)

- **Use [[🏛 CMDS Head Quarter]]**: For navigation
	- Quick access to all 91 subcategories

- **Use [[🏛 CMDS Guide]]**: For standards compliance
	- Required Properties format
	- Standard note types
	- File naming conventions

**Remember**: This file (CLAUDE.md) is **Claude Code specific**. For other AI agents, use **AGENTS.md**.

## File Creation Rules

@.claude/rules/file-creation-rules.md

## Directory Structure

@.claude/rules/directory-structure.md

---

## CMDS-Specific Conventions

### Hierarchy System
- 🏛 - Home/Guide notes (top level)
- 📖 - 1st level CMDS (100-900 series)
- 📚 - 2nd level CMDS (N01-N99)
- (No icon) - 3rd level (detailed topics)

### File Prefixes
- 📎 - Web Clips
- 🏷 - Index
- 📦 - Review
- 🔖 - Personal idea outputs
- 📜 - Others' idea outputs
- 📈 - Code/Syntax
- 🎹 - Music
- 📘 - Books/Reference

### Note Types (type property)
Most common types in the vault:
- `note` - General notes (459+)
- `terminology` - Term definitions (130+)
- `research-pipeline` - Research pipeline documents (124+)
- `meeting` - Meeting notes (160+)
- `people` - People profiles (93+)
- `curriculum` - Course curriculum (82+)
- `channel` - YouTube/Blog/Newsletter 채널 프로필 (101+)
- `CMDS` - CMDS index pages (replaces traditional MOC concept)
- `api` - API documentation (97+)
- `moc` - Map of Content (85+)
- `manuscript` - Manuscripts and drafts (66+)

## Obsidian-Specific Guidelines

### Markdown Files
- Always use wikilinks `[[]]` for internal references, NOT markdown links
- Include YAML frontmatter for metadata (see @.claude/rules/frontmatter-standard.md)
- Standard frontmatter fields:
	- `type:` - Note type/category (see types above)
	- `aliases:` - Alternative names (array format)
	- `author:` - Author information (array format with quoted wikilinks)
	- `date created:` - Creation timestamp (YYYY-MM-DD format)
	- `date modified:` - Last modification (YYYY-MM-DD format)
	- `tags:` - Relevant tags (array format)
	- `CMDS:` - CMDS category reference (quoted wikilink if used)
	- `index:` - Index reference (quoted wikilink if used)
	- `status:` - unread/reading/inProgress/completed/archived

### Note Templates
Templates are located in `90. Settings/91. Templates/`
Key templates include:
- `Template_00. Basic Note.md` - Basic note structure
- `Template_01. Daily Note.md` - Daily journal
- `Template_05. Meeting Minutes.md` - Meeting notes
- `Template_20. Research Note.md` - Research documentation
- `Template_51. People.md` - People profiles
- `Template_80. AI Summary.md` - AI-generated summaries
- `Template_90. CMDS MOC.md` - Map of Content

### Special Characters in Titles
The vault uses emoji prefixes systematically:
- `🏛` - Main index/guide notes (CMDS Guide, CMDS Head Quarter)
- `📖` - Category collections (100-900 series)
- `📚` - Subcollections (2nd level)
- `🏷` - Tag/index pages

## Key Integration Points

### Main Hub Notes
- [[🏛 CMDS Head Quarter]] - Central navigation hub with 9 categories
- [[🏛 CMDS Guide]] - Properties standardization and operational guidelines

### AI Integration
- ChatGPT custom GPTs linked in CMDS Head Quarter
- Claude integration via Claude Code directory
- System prompts in `90. Settings/94. System Prompts/`

### Automation
- n8n workflows for automation
- Obsidian Webhook integration
- Various API integrations (OpenAI, Anthropic, Google)

## Obsidian CLI (v1.12+)

> **📖 Full Reference**: [[Obsidian CLI]] | **📘 실전 가이드**: [[Obsidian CLI 사용 가이드 (CMDS)]]

Obsidian CLI는 터미널에서 Obsidian을 직접 제어하는 명령줄 인터페이스입니다.
**Claude Code에서 `obsidian` 명령을 Bash 도구로 호출하여 Obsidian 네이티브 기능을 활용할 수 있습니다.**

### 요구사항
- Obsidian 1.12+ (Early Access, Catalyst 필요)
- Settings → General → CLI 활성화
- Obsidian 앱 실행 중이어야 함

### Claude Code에서 사용 시 주의사항
- `obsidian` 명령은 Bash 도구로 호출
- 볼트 타겟팅: `obsidian vault=CMDSPACE_Local_MBP <command>`
- 파일 타겟팅: `file=<name>` (wikilink 방식) 또는 `path=<경로>` (볼트 루트 기준)
- 출력 복사: `--copy` 플래그

### 자주 쓰는 CLI 명령 (Quick Reference)

```bash
# --- 읽기/검색 ---
obsidian read file=<name>                          # 파일 내용 읽기
obsidian search query="<text>" format=json          # 볼트 검색
obsidian tags all counts sort=count                 # 태그 통계
obsidian properties all counts sort=count           # 프로퍼티 통계
obsidian backlinks file=<name> counts               # 백링크 조회
obsidian outline file=<name> format=tree            # 목차 조회
obsidian tasks daily todo                           # 오늘 미완료 태스크

# --- 생성/편집 ---
obsidian create name=<name> template=<template> silent  # 템플릿으로 노트 생성
obsidian append file=<name> content="<text>"            # 내용 추가
obsidian prepend file=<name> content="<text>"           # frontmatter 뒤에 삽입
obsidian daily:append content="- [ ] <task>" silent     # 데일리 노트에 태스크 추가
obsidian property:set name=<key> value=<val> file=<name> # 프로퍼티 설정
obsidian property:remove name=<key> file=<name>          # 프로퍼티 제거

# --- 분석 ---
obsidian vault info=files                           # 볼트 파일 수
obsidian orphans total                              # 고아 노트 수
obsidian unresolved verbose                         # 미해결 링크
obsidian deadends total                             # 아웃링크 없는 노트 수

# --- 플러그인 ---
obsidian plugins filter=community versions          # 커뮤니티 플러그인 목록
obsidian plugin:reload id=<plugin-id>               # 플러그인 리로드

# --- 개발자 ---
obsidian eval code="<javascript>"                   # JS 실행 (app.vault 등 접근)
obsidian dev:screenshot path=<filename>             # 스크린샷
obsidian dev:console level=error                    # 콘솔 에러 확인
```

### CLI vs 파일 직접 조작 가이드

| 작업 | CLI 사용 | 파일 직접 조작 |
|------|---------|-------------|
| 프로퍼티 수정 | `property:set` ✅ (안전) | Edit 도구 (YAML 직접 편집) |
| 내용 추가 | `append`/`prepend` ✅ | Edit/Write 도구 |
| 노트 생성 (템플릿) | `create template=` ✅✅ | Write 도구 (수동 복제) |
| 검색 | `search` ✅ (Obsidian 인덱스) | Grep 도구 (파일 시스템) |
| 백링크/링크 분석 | `backlinks`/`orphans` ✅✅ | 불가능 |
| Obsidian API 접근 | `eval` ✅✅ | 불가능 |

---

## Vault Commands

### Note Creation with Proper Metadata
```bash
cat > "00. Inbox/$(date +%Y-%m-%d)-new-note.md" << 'EOF'
---
type: note
aliases: []
author:
  - "[[{your-name}]]"
date created: $(date +%Y-%m-%d)
date modified: $(date +%Y-%m-%d)
tags: []
CMDS:
index:
status:
---

# Title

EOF
```

### Vault Analysis Commands
```bash
find . -name "*.md" -type f | wc -l

grep -L "^type:" **/*.md 2>/dev/null | head -20

grep -h "^type:" **/*.md | sort | uniq -c | sort -rn

find . -name "*.md" -mtime -7 -type f | head -20
```

<!-- DYNAMIC: 아래 내용은 주기적으로 갱신됩니다. 검증이 필요할 수 있습니다. -->

## Critical Workflow Rules

1. **Code Output Location**: ALL code MUST go to `00. Inbox/03. AI Agent/{environment subfolder}/`
2. **Required Properties**: Every note needs 6 fields: type, aliases, author, date created, date modified, tags
3. **Properties v2.0 Standards**:
	- Dates: ISO 8601 (YYYY-MM-DD)
	- Author: `[[{your-name}]]` wikilink format
	- Status: Use standard 5 values only
	- CamelCase: myRate, totalPage (⚠️ `rating` 사용 금지 → 반드시 `myRate`)
4. **CMDS Hierarchy**: 🏛 (top) → 📖 (100-900) → 📚 (N01-N99) → no icon (details)
5. **Vault Scale**: 10,000+ notes with established patterns - respect existing conventions

## Key Obsidian Plugins

The vault uses 120+ plugins. Most important ones:
- **Dataview**: Dynamic queries and data aggregation
- **Copilot**: AI-powered writing assistance
- **Smart Connections**: AI-based note linking
- **Excalidraw/Excalibrain**: Visual thinking and diagramming
- **Chronology**: Timeline visualization
- **Calendar**: Date-based note organization
