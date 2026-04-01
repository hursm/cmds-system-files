# Frontmatter Standard (Required Properties)

Every note in this vault MUST include these 6 required properties:

```yaml
---
type:           # Note type (note, meeting, people, terminology, curriculum, channel, CMDS, etc.)
aliases: []     # Alternative names (array format)
author:
  - "[[{your-name}]]"  # Author as quoted wikilink array
date created:   # YYYY-MM-DD or YYYY-MM-DDTHH:mm (ISO 8601)
date modified:  # YYYY-MM-DD or YYYY-MM-DDTHH:mm (ISO 8601)
tags: []        # Relevant tags (array format)
---
```

## Rules

1. **Wikilinks in YAML must be quoted**: `"[[link]]"` not `[[link]]`
2. **Date format**: Always ISO 8601 — `YYYY-MM-DD` or `YYYY-MM-DDTHH:mm`
3. **Array format**: Use hyphen + space for arrays (author, tags, aliases)
4. **CamelCase for compound words**: `myRate`, `totalPage`, `startReadDate` (⚠️ `rating` 사용 금지 → 반드시 `myRate`)
5. **Status values** (5 options): `unread` / `reading` / `inProgress` / `completed` / `archived`

## Optional Properties

- `CMDS:` — CMDS category reference (quoted wikilink)
- `index:` — Index reference (quoted wikilink)
- `status:` — One of 5 standard values above
