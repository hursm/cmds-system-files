---
date created: 2025-09-27T17:53
date modified: 2026-01-18T16:55
tags:
  - CMDS
  - system
---
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **📌 Related System Files (5 Core Files)**
> - @CMDS.md → [[CMDS.md]] - System philosophy & user context (for ALL LLMs)
> - @AGENTS.md → [[AGENTS.md]] - Technical guide for other AI agents (Gemini, Codex)
> - @🏛 CMDS Head Quarter → [[🏛 CMDS Head Quarter]] - Navigation hub (for User)
> - @🏛 CMDS Guide → [[🏛 CMDS Guide]] - Standards & templates (for User + AI)

## Project Overview

This is an Obsidian vault for the CMDSPACE knowledge management system created by Yohan Koo. It implements the CMDS framework - a comprehensive Personal Knowledge Management (PKM) system with 9 major categories (100-900 series) and follows the CMDS Process: Connect → Merge → Develop → Share.

## 💻 Working Environments

This vault is accessed from two different Mac environments:

### Primary Environment (MacBook Pro) ✅
**Base Path**: `/Users/yohankoo/Local Obsidian_MBP/CMDSPACE_Local_MBP`

**System**: MacBook Pro (16-inch)
**Status**: Primary (Most Frequently Used)
**Usage**: Main development and knowledge management workstation

### Secondary Environment (Mac Studio)
**Base Path**: `/Users/yohankoo/Obsidian_Local/CMDSPACE_Studio_Local_Org`

**System**: Mac Studio
**Status**: Secondary
**Usage**: Desktop workstation for heavy processing tasks

### Important Notes:
- All relative paths in this document (e.g., `00. Inbox/03. Claude Code/`) are relative to the base path above
- When switching between environments, Claude Code will automatically use the appropriate base path
- The vault structure and CMDS system remain identical across both environments
- Cloud sync ensures consistency between the two locations

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
  - "[[Yohan Koo]]"
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
	- "[[Yohan Koo]]"  # ← TAB used - WRONG!
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
3. **Code output location**: ALL code → `00. Inbox/03. Claude Code/`
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
	- Code output location (`00. Inbox/03. Claude Code/`)

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
  - `01. Daily Notes/` - Daily journal entries
  - `02. Automation/` - n8n, Make.com automation
  - `03. Claude Code/` - **PRIMARY WORKING DIRECTORY** for all code outputs
  - `04. Excalidraw/` - Visual diagrams and drawings
  - `05. Canvas/` - Canvas notes
  - `06. GenAI Chats/` - AI conversation logs
  - `07. Clippings/` - Web clippings and external content
- `10. CMDS Process/` - Process documentation (Connect→Merge→Develop→Share)
- `20. Literature Notes/` - Reading notes and literature reviews
- `30. Permanent Notes/` - Permanent, refined notes
- `40. Docs/` - Technical documentation
- `50. Assets/` - Images and media files
- `60. Preferences/` - User preferences
- `70. Collections/` - Organized collections (People, Meetings, Curriculum)
- `80. References/` - Reference materials
- `90. Settings/` - System settings and templates

## ✅ Pre-Flight Checklist (Before Every Write/Edit)

**Every time you create or edit a .md file, verify:**

- [ ] **YAML frontmatter uses 2 SPACES** (not tabs)
- [ ] **Markdown body uses TAB** (not spaces)
- [ ] **Wikilinks in YAML are quoted**: `"[[link]]"` not `[[link]]`
- [ ] **Arrays use proper format**: hyphen + space + value
  ```yaml
  author:
    - "[[Yohan Koo]]"    # ← Correct
  ```
- [ ] **Dates use ISO 8601**: `YYYY-MM-DD` format
- [ ] **File saved in correct location**: Code → `00. Inbox/03. Claude Code/`
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
**ALL code-related outputs MUST be saved in:** `00. Inbox/03. Claude Code/`

### Subdirectory Structure
```
00. Inbox/03. Claude Code/
├── scripts/           # Standalone scripts
├── projects/          # Multi-file projects
├── templates/         # Reusable templates
├── experiments/       # Experimental code
└── outputs/          # Generated results
```

### Multi-File Project Folder Rule

When creating projects with multiple related files (e.g., website with HTML/CSS/JS, lecture materials with multiple notes):
1. **FIRST** create an intermediate folder with descriptive name
2. **THEN** create all related files inside that folder
3. Folder naming: `YYYY-MM-DD-project-name/` (e.g., `2026-01-18-한림대-강의/`)

Example structure:
```
00. Inbox/03. Claude Code/
└── 2026-01-18-project-name/
    ├── index.html
    ├── styles.css
    ├── script.js
    └── README.md
```

**Never** scatter related project files directly in `03. Claude Code/` root.

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
- `[[Yohan Koo]]` - Links to people note
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

## Vault Commands

### Note Creation with Proper Metadata
```bash
cat > "00. Inbox/$(date +%Y-%m-%d)-new-note.md" << 'EOF'
---
type: note
aliases: []
author:
  - "[[Yohan Koo]]"
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

1. **Code Output Location**: ALL code MUST go to `00. Inbox/03. Claude Code/`
2. **Required Properties**: Every note needs 6 fields: type, aliases, author, date created, date modified, tags
3. **Properties v2.0 Standards**:
   - Dates: ISO 8601 (YYYY-MM-DD)
   - Author: `[[Yohan Koo]]` wikilink format
   - Status: Use standard 5 values only
   - CamelCase: myRate, totalPage
4. **CMDS Hierarchy**: 🏛 (top) → 📖 (100-900) → 📚 (N01-N99) → no icon (details)
5. **Vault Scale**: 5,344+ notes with established patterns - respect existing conventions

## Key Obsidian Plugins

The vault uses 120+ plugins. Most important ones:
- **Dataview**: Dynamic queries and data aggregation
- **Copilot**: AI-powered writing assistance
- **Smart Connections**: AI-based note linking
- **Excalidraw/Excalibrain**: Visual thinking and diagramming
- **Chronology**: Timeline visualization
- **Calendar**: Date-based note organization
