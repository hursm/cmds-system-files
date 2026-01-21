---
type: CMDS
aliases:
  - guide
author:
  - "[[Yohan Koo]]"
date created: 2025-09-15T23:39
date modified: 2026-01-02T17:00
tags: [index, NoteClass, maps, SystemPrompt, guideline]
links:
  - "[[🏛 CMDS Head Quarter|CMDS HQ]]"
---

# CMDS Guide

> 📌 **Version 2.1** - Properties standardization and system improvement
> Last Updated: 2026-01-02

## Properties
### Required Properties
All notes must include these 6 required properties:
```yaml
---
type:           # Note type (see standard types below)
aliases: []     # Aliases (array format)
author:
  - "[[Yohan Koo]]"  # Author (wikilink format)
date created:   # Creation date (YYYY-MM-DDTHH:mm:ss)
date modified:  # Modified date (YYYY-MM-DDTHH:mm:ss)
tags: []        # Tags (array format)
---
```

### Standard Properties Definition
#### Date Related
- `date created` - Creation date (YYYY-MM-DDTHH:mm:ss)
- `date modified` - Modified date (YYYY-MM-DDTHH:mm:ss)
- `date` - Event/meeting date (YYYY-MM-DD)
- `publish_date` - Publication date (YYYY-MM-DD)
- `year` - Year (YYYY)
> ⚠️ **Standard Rule**: All dates use ISO 8601 format (YYYY-MM-DD)

#### Author and Relations
- `author: [[Yohan Koo]]` - Always use wikilink format
- `attendees: []` - Attendee list (wikilink array)
- `organization: [[Organization Name]]` - Organization (wikilink)

#### Classification and Status
- `type` - Note type (see standard type list below)
- `CMDS` - CMDS category link (e.g., `[[📚 620 Generative AI]]`)
- `index` - Index reference (e.g., `[[🏷 Meeting Notes]]`)
- `status` - Status value
	- ✅ Standard values: `unread` | `reading` | `inProgress` | `completed` | `archived`

#### Evaluation and Measurement
- `myRate` - Rating (1-5 scale, number)
- `totalPage` - Total pages (camelCase)
- `views` - View count

#### Links and References
- `aliases: []` - Aliases (array format)
- `tags: []` - Tags (array format)
- `links` - Related links
- `source` - Source
- `source_url` - Source URL
- `MOC` - Map of Content reference

### Standard Type List
#### Primary Note Types
- `note` - General notes
- `terminology` - Term definitions
- `meeting` - Meeting minutes
- `people` - People profiles
- `curriculum` - Lecture curriculum
- `memo` - Memos
- `class` - Class related
- `manuscript` - Manuscripts/drafts
- `daily-note` - Daily notes
- `article` - Articles
- `review` - Reviews/research critiques
- `project` - Projects
- `zettel` - Zettelkasten notes

#### Structure/Organization Types
- `CMDS` - CMDSPACE index
- `organization` - Organizations/institutions
- `portal` - Portal pages
- `documentation` - Documentation/guides
- `index` - Index
- `moc` - Map of Content

#### Content Types
- `books` - Books
- `research-review` - Research reviews
- `idea` - Ideas
- `resource` - Resources
- `product` - Products/services

### Tags
- Tags are flexible
- Nested tags examples:
	- `#Author/Koo`
	- `#Guide/TagWriting`
	- `#Guide/TOCWriting`

## Collections
### CMDS
- [[🏛 CMDS Head Quarter]]
- [[🏛 CMDS Guide]]

### Index
#index #NoteClass #maps
- [[🏷 Guideline]]
- [[🏷 Daily Notes]]
- [[🏷 Research Notes]]
- [[🏷 Project Notes]]
- [[🏷 Lecture Notes]]
- [[🏷 Review Notes]]
- [[🏷 Draft Article]]
- [[🏷 Web Clips]]
- [[🏷 Waypoint]]
- [[🏷 Meeting Notes]]
- [[🏷 People]]
- [[🏷 Organization]]
- [[🏷 Prompts]]
- [[🏷 Syntax and Codes]]
- [[🏷 Recordings]]

### Backlinks
- Backlinks as far as cognitive capacity allows [[]]
- No need to do everything at once
- Can use Gen AI for automatic linking
	- Smart Composer - YAML, In-line
	- Claude Code

## CMDS Levels
### Hierarchy Structure
- 🏛 - Home, Guide (top level)
- 📖 - 1st level CMDS (100-900 series)
	- Space Collection
	- 1 digit (100-900)
- 📚 - 2nd level CMDS (N01-N99)
	- Spaces
	- 2 digit (N01-N99)
- (No Icon) - 3rd level CMDS
	- Detailed topics as 3rd level CMDS

### CMDS Level Example
```
📚 840 Lectures
├── 840.01 University Courses
│   ├── 840.01-A University A
│   │   ├── 840.01-A1 2024-1
│   │   │   └── [[AI Fundamentals and Applications]]
│   │   └── 840.01-A2 2024-2
│   │       └── AI Convergence Research Methods
│   └── 840.01-B University B
```

## Filename Conventions
### Prefixes
#### Wis' Rule
- `u.` - usecase #example
- `f.` - feature #operation
- `p.` - product #service

#### Input
- 📎 - Web Clips (W@)
- 🌿 - Readwise (WW@)
- 📘 - Books, Reference `#📚Book`

#### Process
- 🏷 - Index (E@)
- 📦 - Review (EE@)
- 📐 - Variables (EEEE@)

#### Output
- 🔖 - Output from own ideas (R@)
- 📜 - Output from others' ideas (RR@)
- 📈 - Code and Syntax (RRR@)
- 🎹 - Music (RRRR@)
- 🏙 - Canvas (F@)

#### References
- 📕 - Bible (EEE@)

### Suffixes
#### By Service
- `.obsidian`
- `.python`
- `.chatgpt`
- `.claude`
- `.midjourney`

#### By Purpose
- `.meeting`
- `.portal`

## Folder Structure
```
00. Inbox/                      # Temporary storage and processing
├── 01. Daily Notes/
├── 02. Automation/             # n8n, Make.com automation
├── 03. Claude Code/            # ⭐ Code work only (PRIMARY)
├── 04. Excalidraw/             # Diagrams
├── 05. Canvas/                 # Canvas notes
├── 06. GenAI Chats/            # AI conversation logs
├── 07. Clippings/              # Web clippings
├── 08. Unlisted/               # Uncategorized
└── 09. Legacy/                 # Legacy content

10. CMDS Process/               # CMDS process workflow
├── 11. Connect/                # Learning #capture
├── 12. Merge/                  # Connect to my topics #Areas #organize
├── 13. Develop/                # #distill
└── 14. Share/                  # Completed outputs #express

20. Literature Notes/           # Literature notes and reviews
├── 21. Lit Notes (Zotero)/     # Zotero linked literature
├── 22. Reviews/                # Reviews and analysis
├── 24. Web Articles/           # Web articles
├── 28. Flashcards/             # Flashcards
└── 29. Terminologies/          # Terminology notes

30. Permanent Notes/            # Permanent notes (Evergreen)
├── 33. Essay/                  # Essays
├── 34. Prompt and Syntax/      # Prompts and syntax
└── 39. Guideline/              # Guidelines

40. Docs/                       # Technical Documentation
├── 41. Official Docs/          # Official docs, API guides, product manuals
├── 42. AI Generated/           # AI generated technical docs
├── 43. My Docs/                # User-created technical docs
└── 44. Transcripts/            # Transcripts

50. Assets/                     # Media and assets
├── 51. Prompt/                 # Prompt assets
├── 52. Workflow/               # Workflow assets
└── 59. Obsidian Web Clipper/   # Web clipper templates

60. Preferences/                # Personal preferences and lifestyle

70. Collections/                # Resources collection
├── 71. People/                 # People database
├── 72. Organization/           # Organizations/institutions
├── 74. Meetings/               # Meeting minutes
├── 76. Curriculum/             # Lecture curriculum
├── 77. Class/                  # Class management
├── 78. Bases/                  # Database structures
└── 79. Portal/                 # Portal pages

80. References/                 # Reference materials and sources
├── 81. Attachment/             # File attachments
├── 82. Web Articles/           # Web articles
├── 83. References/             # General references
├── 84. References (Zotero)/    # Zotero references
└── 85. References (Book)/      # Book references

90. Settings/                   # System settings and management
├── 91. Templates/              # Note templates
├── 92. Templates (archived)/   # Archived templates
├── 93. Generated Text/         # AI generated text
├── 94. System Prompts/         # AI system prompts
├── 95. Fonts/                  # Font files
├── 96. Index/                  # Index files
├── 97. File Class/             # File classification
├── 98. Format/                 # Format definitions
└── 99. Others/                 # Other settings
```

## Properties Template Examples
### Basic Note Template
```yaml
---
type: note
aliases: []
author:
  - "[[Yohan Koo]]"
date created: 2025-01-09T14:30
date modified: 2025-01-09T14:30
tags: []
CMDS: 
index: 
status: 
---
```

### Meeting Template
```yaml
---
type: meeting
aliases: []
author:
  - "[[Yohan Koo]]"
date created: 2025-01-09T09:00
date: 2025-01-09
attendees:
  - "[[Attendee 1]]"
  - "[[Attendee 2]]"
organization: "[[Organization Name]]"
CMDS: "[[📚 831 Consulting]]"
index: "[[🏷 Meeting Notes]]"
status: inProgress
tags: [meeting]
---
```

### Research Note Template
```yaml
---
type: research-review
aliases: []
author:
  - "[[Yohan Koo]]"
date created: 2025-01-09T16:45
title: 
source: 
source_url: 
doi: 
keywords: []
CMDS: "[[📚 820 Research]]"
index: "[[🏷 Research Notes]]"
status: reading
tags: [research]
---
```

### Book Note Template
```yaml
---
type: books
aliases: []
author:
  - "[[Yohan Koo]]"
date created: 2025-01-09T11:20
title: 
subtitle: 
isbn: 
publisher: 
publish_date: 
totalPage: 
myRate: 
status: unread
CMDS: "[[📚 240 Books]]"
index: "[[🏷 Books]]"
tags: [📚Book]
---
```

### People Note Template
```yaml
---
type: people
aliases: []
author:
  - "[[Yohan Koo]]"
date created: 2025-01-09T10:15
email: 
mobile: 
organization: "[[Organization Name]]"
group: 
CMDS: 
index: "[[🏷 People]]"
status: 
tags: [people]
---
```

## Note-taking Guidelines
### Citation Style
#### Book Citation
> [!TIP] _Knowledge Management for the Future_
> Original book content^[Koo, Y. (2021). _Knowledge Management for the Future._ New York: Oxford University Press. p.25.]

#### Paper Citation
> [!ABSTRACT] Knowledge Management in Organizations
> Importance of knowledge management in organizations^[Kim, S., & Lee, H. (2023). The impact of knowledge management. _Journal of Knowledge Management_, 27(4), 1012-1035.]

#### Quote
> [!QUOTE]
> "See you in two weeks."
> — Yohan Koo

## Sync Settings
### Obsidian Sync
- `.obsidian` - macOS, Windows, Android
- `.obsidian_mobile` - iOS, iPadOS

## Version History
- **v2.1** (2025-10-23): Content error and consistency fixes
- **v2.0** (2025-09-15): Properties standardization and system improvement
	- ISO 8601 date format standardization
	- Author field wikilink format standardization
	- Status standard value definition
	- myRate rating standardization
	- totalPage camelCase standardization
	- tags/aliases array format standardization
- **v1.0** (2022-05-25): Initial version

---
*This guide defines the standard Properties system for the CMDSPACE vault. All new notes should follow these rules.*
