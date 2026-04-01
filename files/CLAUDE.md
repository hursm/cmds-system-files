---
type: documentation
aliases:
  - Claude Code Guide
  - CC System File
description: Claude Code 전용 기술 구현 가이드. 파일 생성/편집 규칙, YAML/MD 인덴트 규칙, 볼트 명령어, 코드 출력 경로를 정의한다.
author:
  - "[[{your-name}]]"
date created: 2025-09-27T17:53
date modified: 2026-03-15T21:17
tags:
  - CMDS
  - system
audience: Claude Code
scope: technical-implementation
CMDS: "[[📚 501 Obsidian]]"
index: "[[🏛 CMDS Head Quarter]]"
version: "2.1"
status: completed
---
> **🔄 Last Updated: 2026-03-15** | Backup: `40. Docs/47. CMDS Docs/cmds-system-files/CLAUDE_backup.md`

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **📌 Related System Files (5 Core Files)**
> - @CMDS.md → [[CMDS.md]] - System philosophy & user context (for ALL LLMs)
> - @AGENTS.md → [[AGENTS.md]] - Technical guide for other AI agents (Gemini, Codex)
> - @🏛 CMDS Head Quarter → [[🏛 CMDS Head Quarter]] - Navigation hub (for User)
> - @🏛 CMDS Guide → [[🏛 CMDS Guide]] - Standards & templates (for User + AI)

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
**Base Path**: `{vault-path-secondary}`

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

## ⚠️ CRITICAL RULES - READ FIRST

### 🚨 INDENTATION RULES (MOST COMMON MISTAKE)

**Before EVERY Write() or Edit() operation, verify indentation:**

| Section | Indentation | Visual Example |
|---------|-------------|----------------|
| **YAML frontmatter** | **2 SPACES** | `··- "[[link]]"` (· = space) |
| **Markdown body** | **TAB** | `→- List item` (→ = tab) |

#### ✅ CORRECT YAML Frontmatter (2 spaces):
```yaml
---
type: note
aliases:
  - Example Alias
author:
  - "[[{Your Name}]]"
tags:
  - AI
  - knowledge-management
---
```

#### ❌ WRONG YAML Frontmatter (tabs):
```yaml
---
type: note
aliases:
	- Example Alias    # ← TAB used - WRONG!
author:
	- "[[{Your Name}]]"  # ← TAB used - WRONG!
---
```

#### ✅ CORRECT Markdown Body (tabs):
```markdown
- First level item
	- Second level (TAB)
		- Third level (TAB TAB)
```

#### ❌ WRONG Markdown Body (spaces):
```markdown
- First level item
  - Second level (spaces) - WRONG!
    - Third level (spaces) - WRONG!
```

### Other Critical Rules:
1. **Wikilinks in YAML must be quoted**: `"[[link]]"` not `[[link]]`
2. **Date format**: Always `YYYY-MM-DD` (ISO 8601)
3. **Code output location**: ALL code → `00. Inbox/03. AI Agent/` (environment-specific subfolder)
   - MacBook Pro: `03-1. Claude Code (MBP)/` | Mac Studio: `03-2. Claude Code (Studio)/`
4. **Array format**: Use hyphen + space for arrays (author, tags, aliases)

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

| File                        | Purpose             | Audience    | Focus                                    |
| --------------------------- | ------------------- | ----------- | ---------------------------------------- |
| **🏛 CMDS Head Quarter.md** | Navigation hub      | User        | **WHERE** - Category map, quick links    |
| **🏛 CMDS Guide.md**        | Operational standards | User + AI   | **STANDARDS** - Properties, templates    |

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

- **Use 🏛 CMDS Head Quarter.md**: For navigation
	- Quick access to all 91 subcategories
	- Links to ChatGPT custom GPTs

- **Use 🏛 CMDS Guide.md**: For standards compliance
	- Required Properties format
	- Standard note types
	- File naming conventions

**Remember**: This file (CLAUDE.md) is **Claude Code specific**. For other AI agents, use **AGENTS.md**.

## CMDS Architecture

### Core Categories (100-900 Series)
1. **📖 100 Themes** - Interests, topics, variables, terminologies
2. **📖 200 Literature** - Concepts, frameworks, theories, classics, reviews
3. **📖 300 Data** - Data management, surveys, panel data, LMS
4. **📖 400 Methodologies** - Research methods, statistics, ML, codes/prompts
5. **📖 500 Products** - Tools (Obsidian, Notion, ChatGPT, Claude)
6. **📖 600 Specialties** - KM, Second Brain, Gen AI, productivity
7. **📖 700 Creatives** - YouTube, SNS, music, digital art
8. **📖 800 Outputs** - PhD, articles, lectures, projects, consulting
9. **📖 900 Divisions** - 9 operational divisions

### CMDS Process Workflow
- **Connect**: Idea discovery and connection (100 Themes)
- **Merge**: Literature and knowledge integration (200 Literature)
- **Develop**: Data collection and methodology application (300-600)
- **Share**: Creative work and output dissemination (700-800)

## Directory Structure

### Main Directories
- `00. Inbox/` - Temporary storage and processing area
	- `01. Daily Notes/` - Daily journal entries (01-1. Planners, 01-2. Weekly Notes)
	- `02. Clippings/` - Web clippings (02-1. Literature Notes)
	- `03. AI Agent/` - **PRIMARY WORKING DIRECTORY** for all AI coding outputs
		- `03-1. Claude Code (MBP)/` - Claude Code outputs on MacBook Pro
		- `03-2. Claude Code (Studio)/` - Claude Code outputs on Mac Studio
		- `03-3. OpenClaw (MBP)/` - OpenClaw outputs on MacBook Pro
		- `03-4. OpenClaw (Studio)/` - OpenClaw outputs on Mac Studio
	- `04. Excalidraw/` - Visual diagrams and drawings
	- `05. Canvas/` - Canvas notes
	- `06. Automation/` - Automation workflows (06-1. Make.com, 06-2. n8n Lecture, 06-3. STT)
	- `06. GenAI Chats/` - GenAI 대화 기록
	- `07. App Sync/` - External app sync (07-1. Claude, 07-2. Antigravity, 07-3. Bear Notes)
	- `08. Unlisted/` - Unlisted items
	- `09. Legacy/` - Legacy and archived content
- `10. CMDS Process/` - Process documentation (Connect→Merge→Develop→Share)
- `20. Literature Notes/` - Reading notes and literature reviews (외부 지식 내재화)
- `30. Permanent Notes/` - Permanent, refined notes (정제된 개인 지식)
- `40. Docs/` - Technical documentation (업무 문서/기록)
- `50. Assets/` - Reusable resources and tools (재사용 자원)
- `60. Collections/` - Entity management (People, Meetings, Preferences)
- `70. Outputs/` - Final deliverables (최종 산출물: Published, Presentations, Courses, Curriculum, Projects)
- `80. References/` - Reference materials (참조 자료)
- `90. Settings/` - System settings and templates

## ✅ Pre-Flight Checklist (Before Every Write/Edit)

**Every time you create or edit a .md file, verify:**

- [ ] **YAML frontmatter uses 2 SPACES** (not tabs)
- [ ] **Markdown body uses TAB** (not spaces)
- [ ] **Wikilinks in YAML are quoted**: `"[[link]]"` not `[[link]]`
- [ ] **Arrays use proper format**: hyphen + space + value
  ```yaml
  author:
    - "[[{Your Name}]]"    # ← Correct
  ```
- [ ] **Dates use ISO 8601**: `YYYY-MM-DD` format
- [ ] **File saved in correct location**: Code → `00. Inbox/03. AI Agent/{environment subfolder}/`
  - MBP + Claude Code → `03-1. Claude Code (MBP)/`
  - Studio + Claude Code → `03-2. Claude Code (Studio)/`
- [ ] **Filename follows convention**: `YYYY-MM-DD-description.ext`

**Common mistakes to avoid:**
- ❌ Using tabs in YAML frontmatter
- ❌ Using spaces in markdown body indentation
- ❌ Forgetting quotes around wikilinks in YAML
- ❌ Wrong date format (MM/DD/YYYY, YYYY.MM.DD, etc.)

---

## File Creation Rules

> ⚠️ **INDENTATION**: See "CRITICAL RULES" section above for YAML (2 spaces) vs Markdown (TAB) rules.

### Working Directory
**ALL code-related outputs MUST be saved in:** `00. Inbox/03. AI Agent/` under the appropriate **environment subfolder**.

### Environment-Specific Subfolders
```
00. Inbox/03. AI Agent/
├── 03-1. Claude Code (MBP)/     # Claude Code on MacBook Pro ← PRIMARY
├── 03-2. Claude Code (Studio)/  # Claude Code on Mac Studio
├── 03-3. OpenClaw (MBP)/        # OpenClaw on MacBook Pro
└── 03-4. OpenClaw (Studio)/     # OpenClaw on Mac Studio
```

**Auto-detection**: Determine subfolder by checking:
- **Agent**: Claude Code → `03-1` or `03-2` | OpenClaw → `03-3` or `03-4`
- **Machine**: MacBook Pro (`{home-path}/Local Obsidian_MBP/`) → MBP | Mac Studio (`{home-path}/Obsidian_Local/`) → Studio

### Multi-File Project Folder Rule

When creating projects with multiple related files (e.g., website with HTML/CSS/JS, lecture materials with multiple notes):
1. **FIRST** create an intermediate folder with descriptive name inside the environment subfolder
2. **THEN** create all related files inside that folder
3. Folder naming: `YYYY-MM-DD-project-name/` (e.g., `2026-01-18-한림대-강의/`)

Example structure:
```
00. Inbox/03. AI Agent/03-1. Claude Code (MBP)/
└── 2026-01-18-project-name/
    ├── index.html
    ├── styles.css
    ├── script.js
    └── README.md
```

**Never** scatter related project files directly in `03. AI Agent/` root or environment subfolder root.

### File Naming Convention
- Include date: `YYYY-MM-DD-description.ext`
- Use descriptive names
- Examples:
	- `2025-01-09-data-analysis.py`
	- `2025-01-09-meeting-summary.md`

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
- `note` - General notes (142+)
- `terminology` - Term definitions (101+)
- `meeting` - Meeting notes (80+)
- `people` - People profiles (59+)
- `curriculum` - Course curriculum (36+)
- `CMDS` - CMDS index pages (replaces traditional MOC concept)

## Obsidian-Specific Guidelines

### Wikilinks (Internal Links)
**CRITICAL**: Obsidian uses `[[double brackets]]` for internal file linking
- Basic link: `[[Note Name]]`
- Link with alias: `[[Note Name|Display Text]]`
- Link to heading: `[[Note Name#Heading]]`
- Link to block: `[[Note Name^block-id]]`
- Embed file: `![[Note Name]]`
- Embed image: `![[image.png]]`

Examples in this vault:
- `[[🏛 CMDS Head Quarter]]` - Links to main hub
- `[[📚 620 Generative AI]]` - Links to CMDS category
- `[[{Your Name}]]` - Links to people note
- `[[🏷 Meeting Notes]]` - Links to index page

### Markdown Files
- Always use wikilinks `[[]]` for internal references, NOT markdown links
- **CRITICAL - Indentation Rules**:
	- **Markdown content (lists, nested items)**: Use TAB for indentation
	- **YAML frontmatter**: Use 2 spaces (NOT tabs) for indentation
- Include YAML frontmatter for metadata
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

### Important YAML Rules
- **Wikilinks in YAML must be quoted**: When using `[[]]` links in YAML fields, always wrap them in double quotes
	- ✅ Correct: `organization: "[[Company Name]]"`
	- ❌ Wrong: `organization: [[Company Name]]`
- **Array fields for multiple values**: Use array format for fields that can have multiple values
	- `author:`, `attendees:`, `aliases:`, `tags:` should use array format
- **YAML indentation**: Use 2 spaces (NOT tabs) for indentation in YAML frontmatter only
- **Markdown body indentation**: Use TAB (NOT spaces) for all markdown content indentation
- **Date format**: Always use ISO 8601 (YYYY-MM-DD) for date fields
- **CamelCase for compound words**: Use camelCase for fields like `totalPage`, `myRate`, `startReadDate`

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
- `🏛 CMDS Head Quarter.md` - Central navigation hub with 9 categories and ChatGPT GPT links
- `🏛 CMDS Guide.md` - Properties standardization and operational guidelines

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
  - "[[{Your Name}]]"
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

## Critical Workflow Rules

1. **Code Output Location**: ALL code MUST go to `00. Inbox/03. AI Agent/{environment subfolder}/`
2. **Required Properties**: Every note needs 6 fields: type, aliases, author, date created, date modified, tags
3. **Properties v2.0 Standards**:
	- Dates: ISO 8601 (YYYY-MM-DD)
	- Author: `[[{Your Name}]]` wikilink format
	- Status: Use standard 5 values only
	- CamelCase: myRate, totalPage
4. **CMDS Hierarchy**: 🏛 (top) → 📖 (100-900) → 📚 (N01-N99) → no icon (details)
5. **Vault Scale**: 7,660+ notes with established patterns - respect existing conventions

## Key Obsidian Plugins

The vault uses 120+ plugins. Most important ones:
- **Dataview**: Dynamic queries and data aggregation
- **Copilot**: AI-powered writing assistance
- **Smart Connections**: AI-based note linking
- **Excalidraw/Excalibrain**: Visual thinking and diagramming
- **Chronology**: Timeline visualization
- **Calendar**: Date-based note organization
