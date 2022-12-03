# Markdown Cornell Syntax Highlighting

settings.json

```json
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": "cornell.question",
                "settings": {
                    "foreground": "#D19000",
                }
            },
            {
                "scope": "cornell.answer",
                "settings": {
                    "foreground": "#D19000",
                }
            },
            {
                "scope": "supermemo.cloze",
                "settings": {
                    "foreground": "#F04040",
                }
            },
            {
                "scope": "supermemo.cloze.hints",
                "settings": {
                    "foreground": "#C04000",
                }
            },
            {
                "scope": "markup.italic.markdown",
                "settings": {
                    "foreground": "#00A000",
                }
            },
            {
                "scope": "punctuation.definition.italic.markdown",
                "settings": {
                    "foreground": "#00A000",
                }
            },
        ]
    },
```

## Building

```bash
vsce package
```

## Example

Q: do normal markdown syntax, such as *italic*, **bold**, working in Q&A?

A: yes, {{syntax *highlight*}} for {{**normal** markdown}}(such as *italic*), or **bold** is not affected.

![example](data/example.png)
