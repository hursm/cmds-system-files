---
date created: 2026-01-02T16:30
date modified: 2026-01-24T00:35
tags:
  - CMDS
  - system
---
> **🔄 Last Updated: 2026-01-24** | Backup: `00. Inbox/03. AI Agent/cmds-system-files/AGENTS_backup.md`

# AGENTS.md

This file provides guidance to AI coding agents (Gemini CLI, Codex, Cursor, Windsurf, etc.) when working with this Obsidian vault.

> **📌 Related System Files (5 Core Files)**
> - @CLAUDE.md → [[CLAUDE.md]] - Claude Code specific instructions
> - @CMDS.md → [[CMDS.md]] - System philosophy & user context (for ALL LLMs)
> - @🏛 CMDS Head Quarter → [[🏛 CMDS Head Quarter]] - Navigation hub (for User)
> - @🏛 CMDS Guide → [[🏛 CMDS Guide]] - Standards & templates (for User + AI)

---

## Project Overview

This is an Obsidian vault for the **CMDSPACE (커맨드스페이스)** knowledge management system created by 구요한 (Yohan Koo). It implements the CMDS framework - a comprehensive Personal Knowledge Management (PKM) system with 9 major categories (100-900 series).

**Vault Scale**: 5,300+ notes, 120+ plugins, 90+ templates

---

## System Documentation

| File | Purpose | Audience |
|------|---------|----------|
| **AGENTS.md** (this file) | Technical guide for AI coding agents | Gemini CLI, Codex, etc. |
| **CLAUDE.md** | Claude Code specific instructions | Claude Code only |
| **CMDS.md** | System philosophy & user context | All LLM assistants |
| **🏛 CMDS Head Quarter.md** | Navigation hub | User (구요한) |
| **🏛 CMDS Guide.md** | Standards & templates | User + AI |

---

## Critical Rules

### 1. Indentation Rules (YAML vs Markdown)

| Section | Indentation | Example |
|---------|-------------|---------|
| **YAML frontmatter** | **2 SPACES** | `··- "[[link]]"` |
| **Markdown body** | **TAB** | `→- List item` |

### 2. Wikilinks in YAML Must Be Quoted

```yaml
# ✅ Correct
author:
  - "[[구요한]]"
organization: "[[SK Innovation]]"
CMDS: "[[📚 620 Generative AI]]"

# ❌ Wrong
author:
  - [[구요한]]
```

### 3. Required Properties (6 fields)

Every note must include:
```yaml
---
type:           # Note type (note, meeting, people, etc.)
aliases: []     # Alternative names
author:
  - "[[구요한]]"
date created:   # YYYY-MM-DD or YYYY-MM-DDTHH:mm
date modified:  # YYYY-MM-DD or YYYY-MM-DDTHH:mm
tags: []        # Relevant tags
---
```

### 4. Date Format

Always use ISO 8601: `YYYY-MM-DD` or `YYYY-MM-DDTHH:mm`

### 5. Code Output Location

All code-related outputs should be saved in: `00. Inbox/03. AI Agent/`

### 6. Multi-File Project Folder Rule

When creating projects with multiple related files (e.g., website with HTML/CSS/JS, lecture materials with multiple notes):
1. **FIRST** create an intermediate folder with descriptive name
2. **THEN** create all related files inside that folder
3. Folder naming: `YYYY-MM-DD-project-name/` (e.g., `2026-01-18-한림대-강의/`)

Example structure:
```
00. Inbox/03. AI Agent/
└── 2026-01-18-project-name/
    ├── index.html
    ├── styles.css
    ├── script.js
    └── README.md
```

**Never** scatter related project files directly in `03. AI Agent/` root.

---

## Directory Structure

```
00. Inbox/                      # Temporary storage
├── 01. Daily Notes/            # Daily journal (01-1. Planners, 01-2. Weekly Notes)
├── 02. Clippings/              # Web clippings (02-1. Literature Notes)
├── 03. AI Agent/               # Code outputs (PRIMARY)
├── 04. Excalidraw/             # Diagrams
├── 05. Canvas/                 # Canvas notes
├── 06. Automation/             # Automation (Make.com, n8n, STT)
├── 07. App Sync/               # External apps (Claude, Antigravity, Bear Notes)
├── 08. Unlisted/               # Unlisted items
└── 09. Legacy/                 # Legacy content

10. CMDS Process/               # Connect→Merge→Develop→Share
20. Literature Notes/           # Reading notes
30. Permanent Notes/            # Evergreen content
40. Docs/                       # Technical documentation
50. Assets/                     # Media files
60. Collections/                # Entity management (People, Meetings, Preferences)
70. Outputs/                    # Final deliverables (Published, Presentations, Courses, Curriculum, Projects)
80. References/                 # Reference materials
90. Settings/                   # Templates, System Prompts
```

---

## CMDS Categories (100-900)

| Category | Name | Purpose |
|----------|------|---------|
| 📖 100 | Themes | Interests, topics, variables, terminologies |
| 📖 200 | Literature | Concepts, frameworks, theories, reviews |
| 📖 300 | Data | Data management, surveys, databases |
| 📖 400 | Methodologies | Research methods, statistics, ML, codes |
| 📖 500 | Products | Tools (Obsidian, ChatGPT, Claude, etc.) |
| 📖 600 | Specialties | KM, Second Brain, Gen AI, productivity |
| 📖 700 | Creatives | YouTube, SNS, music, digital art |
| 📖 800 | Outputs | PhD, articles, lectures, consulting |
| 📖 900 | Divisions | 9 operational divisions |

### Hierarchy System

- 🏛 - Home/Guide (top level)
- 📖 - 1st level CMDS (100-900 series)
- 📚 - 2nd level CMDS (N01-N99)
- (No icon) - 3rd level (detailed topics)

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

## File Naming Convention

- Include date: `YYYY-MM-DD-description.ext`
- Examples:
	- `2026-01-02-data-analysis.py`
	- `2026-01-02-meeting-summary.md`

---

## Common Note Types

- `note` - General notes
- `terminology` - Term definitions
- `meeting` - Meeting minutes
- `people` - People profiles
- `curriculum` - Course curriculum
- `CMDS` - CMDS index pages (replaces traditional MOC concept)
- `documentation` - Technical docs

---

## Status Values

Standard status values (5 options):
- `unread` - Not yet processed
- `reading` - Currently reading
- `inProgress` - Work in progress
- `completed` - Finished
- `archived` - Historical reference

---

## File Prefixes

- 📎 - Web Clips
- 🏷 - Index pages
- 📦 - Reviews
- 🔖 - Personal outputs
- 📜 - Others' outputs
- 📈 - Code/Syntax
- 🎹 - Music
- 📘 - Books/Reference

---

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
3. **Check CMDS.md** for user context and workflow patterns
4. **Check 🏛 CMDS Guide.md** for detailed standards and templates

---

**For Claude Code**: See [[CLAUDE.md]] for Claude-specific instructions.
**For LLM Context**: See [[CMDS.md]] for system philosophy and user profile.
