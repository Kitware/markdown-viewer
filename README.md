# markdown-viewer
Tiny utility to render markdown sent as a URL parameter

## Usage

To use the Markdown Viewer, simply append your Markdown text to the URL as a `md` parameter. The Markdown text must be URL-encoded.

### Basic Example

Suppose you have the following Markdown content:

```markdown
# Hello World
This is **Markdown** text.
```

You can URL-encode it and append it to the base URL like this ([link](https://kitware.github.io/markdown-viewer/?md=%23%20Hello%20World%0AThis%20is%20**Markdown**%20text)): 

```
https://kitware.github.io/markdown-viewer/?md=%23%20Hello%20World%0AThis%20is%20**Markdown**%20text
```

### Google Sheets

You can use the formula

```
=HYPERLINK(CONCATENATE("https://kitware.github.io/markdown-viewer/?md=",ENCODEURL(A1)),"show markdown")
```

to construct a URL for displaying markdown content in cell `A1`.
