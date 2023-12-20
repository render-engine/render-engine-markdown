# Render Engine Markdown Parser

This is a parser for the [Markdown markup language](https://www.markdownguide.org).

The underlying parser is [python-markdown2](https://pypi.org/project/markdown2/).

## Installation

You can manually import this with `pip install render-engine-markdown` or in `pip install render-engine[extras]`

## Usage

```python
from render_engine import Site, Collection, Page
from render-engine-markdown import MarkdownPageParser

site = Site()

@site.collection
class Collection:
    pages = [Page(content=“Page1")]
    parser = MarkdownPageParser

site.render()
```

### Parser Settings

These are the options that can be pulled from the page:

| Option | Description |
| --- | --- |
| `markdown_extras` | A list of extensions to use. See [python-markdown2](https://pypi.org/project/markdown2/) for a list of extensions. |

