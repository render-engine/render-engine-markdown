# Markdown Parser

This is a parser for the Markdown markup language. This is the default parser for render_engine pages.

[Markdown](https://www.markdownguide.org) is a lightweight markup language with plain text formatting syntax. It is designed so that it can be converted to HTML and many other formats using a tool by the same name.

The underlying parser is [python-markdown2](https://pypi.org/project/markdown2/).

## Parser Options

These are the options that can be pulled from the page:

| Option | Description |
| --- | --- |
| `markdown_extras` | A list of extensions to use. See [python-markdown2](https://pypi.org/project/markdown2/) for a list of extensions. |

## Quickstart

import the MarkdownPageParser

Render Engine includes the parser in `render_engine.parsers.markdown`
Alternatively, you can import directly from this path

```py
from render_engine.parsers.markdown import MarkdownPageParser
# of from render_engine_markdown import MarkdownPageParser

class MyMarkdownPage(Page):
    Parser = MarkdownPageParser
    content_path = "path_to_your_markdown_file.md"
```
