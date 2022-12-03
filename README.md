# Markdown Cornell Syntax Highlighting

settings.json

```json
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": "cornell.question",
                "settings": {
                    "foreground": "#ff6600",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "cornell.answer",
                "settings": {
                    "foreground": "#ff6600",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "supermemo.cloze",
                "settings": {
                    "foreground": "#FF8000",
                    "fontStyle": "bold"
                }
            }
        ]
    },
```

## Building

```bash
vsce package
```

## Example

Q: what do this extension do?

A: do {{syntax highlight}} for {{cornell}}(which method?) notetaking and {{supermemo Q&A}} with *italic* and **bold** text

do {{syntax highlight}} for {{cornell}}(which method?) notetaking and {{supermemo Q&A}} with *italic* and **bold** text
