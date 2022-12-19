# Markdown Cornell Syntax Highlighting

## Cornell/Supermemo Q&A

Recognize question paragraph and answer marker, and custom question id

* Question marker: q or Q followed by a colon, then a space
  * token id: `cornell.question.marker`
* Question paragraph, token id is `cornell.question`
* Answer  marker: a or A followed by a colon, then a space
  * token id: `cornell.answer`
* question id: some thing like `{#q1234}`, this is automaticall generated
  * token id: `cornell.question.id`

For example:

Q: I am a question? {#q1234}

A: Yes, you are a question.

## Hidden question support

You can hide a question by append a lowercase `h` after `q or Q`, for example

Qh: This is a hidden question?

Hidden question can be used when you want to **cover** a  question, then use the answer as a cue to recall the question.

Hidden question's markder token id is the same as normal question (`cornell.question.marker`), but it's body token id is `cornell.question.hidden`,  by set this token's color to the same as the background's color, you can **hide** it!

## Supermemo cloze highlight

You can mark supermemo clozes using `{{}}`,  this is used for automatically generate supermemo Q&A file for each cloze, rather than extract each cloze manually

Cloze hints is also support, text between `()` followed `{{}}` we recognized as cloze hints

* cloze token id: `supermemo.cloze`
* hints  token id: `supermemo.cloze.hints`

For example:

Q: do normal markdown syntax, such as *italic*, **bold**, working in Q&A? {#q1234}

A: yes, {{syntax *highlight*}} for {{**normal** markdown}}(such as *italic*), or **bold** is not affected.

![example](data/example.png)

## APA Style Lettered List, with extension

Recognize APA style lettered lists (see APA manual, 7th, p190). We also allow single number inside `()`

The token id is `apa.lettered.list`

for example:

> Our sample organization used a waterfall model that featured the following sequential stages: (a) requirements analysis, (b) specification, (c) architecture, (d) design, and (e) deployment.

> Our sample organization used a waterfall model that featured the following sequential stages: (1) requirements analysis, (2) specification, (3) architecture, (4) design, and (5) deployment.

## Color configuration example

```json
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": "cornell.question",
                "settings": {
                    "foreground": "#C0C040",
                }
            },
            {
                "scope": "cornell.question.marker",
                "settings": {
                    "foreground": "#FF8000",
                }
            },
            {
                "scope": "cornell.question.hidden",
                "settings": {
                    "foreground": "#282c34",
                }
            },
            {
                "scope": "cornell.question.id",
                "settings": {
                    "foreground": "#804000",
                }
            },
            {
                "scope": "cornell.answer",
                "settings": {
                    "foreground": "#FF8000",
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
            {
                "scope": "markup.quote.markdown",
                "settings": {
                    "foreground": "#A0A0A0",
                }
            },
            {
                "scope": "apa.lettered.list",
                "settings": {
                    "foreground": "#D19a66",
                }
            }
        ]
    },
```

## Building

```bash
vsce package
```
