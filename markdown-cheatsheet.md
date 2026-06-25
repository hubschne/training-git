# Markdown Cheatsheet

Here are a few simple formatting basics to help you write in Markdown.

## Adding Headers

Use hashtags (`#`) to create headers. The number of hashtags determines the level of the heading:

```md
# Main Title (Level 1)
## Section (Level 2)
### Subsection (Level 3)
#### Sub-subsection (Level 4)
```

## Formatting text

### Italic


### Bold


## Creating Lists


## Adding Links


## Adding Images


## Adding code
## Adding Code

**Inline code** — wrap text in single backticks:

`` `like this` `` → `like this`

**Code blocks** — wrap in triple backticks (optionally add a language name after the opening backticks for syntax highlighting):

````python
def hello():
    print("Hello!")
````

To show *literal* backticks inside inline code, wrap with a longer run of backticks:

`````` `code with a backtick` `` ```
````

A couple of notes:

The reason the wrapping looks fiddly above is the classic markdown chicken-and-egg problem: to *display* backticks you need to surround them with a longer run of backticks. If your cheatsheet doesn't need to explain that escaping trick, you can safely drop the last example and keep it to just inline code + fenced blocks.

I used a four-backtick fence around the whole thing so the triple-backtick examples inside render correctly. If you paste this into an editor that only supports triple backticks, you may need to adjust the outer fence. Want me to trim it down to a more minimal version, or expand it with things like indented code blocks or a list of common language identifiers?
