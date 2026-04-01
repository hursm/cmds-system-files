# Obsidian Wikilink Rules

## Syntax

| Pattern | Usage |
|---------|-------|
| `[[Note Name]]` | Basic link |
| `[[Note Name\|Display Text]]` | Aliased link |
| `[[Note Name#Heading]]` | Link to heading |
| `[[Note Name^block-id]]` | Link to block |
| `![[Note Name]]` | Embed file |
| `![[image.png]]` | Embed image |

## Rules

1. **Always use wikilinks `[[]]`** for internal references, NOT markdown links
2. **Wikilinks in YAML must be quoted**: `"[[link]]"` not bare `[[link]]`
3. **Array fields** (`author:`, `attendees:`, `aliases:`): Use array format with quoted wikilinks

## Examples in This Vault

- `[[🏛 CMDS Head Quarter]]` — Main hub
- `[[📚 620 Generative AI]]` — CMDS category
- `[[{your-name}]]` — People note
- `[[🏷 Meeting Notes]]` — Index page
