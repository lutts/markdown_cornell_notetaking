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
