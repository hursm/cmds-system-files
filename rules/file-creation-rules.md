# File Creation Rules

## Code Output Location

**ALL code-related outputs MUST be saved in:** `00. Inbox/03. AI Agent/` under the appropriate environment subfolder.

| Subfolder | Agent | Machine |
|-----------|-------|---------|
| `03-1. Claude Code (MBP)/` | Claude Code | MacBook Pro |
| `03-2. Claude Code (Studio)/` | Claude Code | Mac Studio |
| `03-3. OpenClaw (MBP)/` | OpenClaw | MacBook Pro |
| `03-4. OpenClaw (Studio)/` | OpenClaw | Mac Studio |

**Auto-detection**: Check base path to determine machine:
- `{home-path}/Local Obsidian_MBP/` → MBP
- `{home-path}/Obsidian_Local/` → Studio

## File Naming Convention

- Include date: `YYYY-MM-DD-description.ext`
- Use descriptive names
- Examples: `2026-01-09-data-analysis.py`, `2026-01-09-meeting-summary.md`

## Multi-File Project Folder Rule

When creating projects with multiple related files:
1. **FIRST** create an intermediate folder: `YYYY-MM-DD-project-name/`
2. **THEN** create all related files inside that folder

```
00. Inbox/03. AI Agent/03-1. Claude Code (MBP)/
└── 2026-01-18-project-name/
    ├── index.html
    ├── styles.css
    └── script.js
```

**Never** scatter related project files directly in subfolder root.
