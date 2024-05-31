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

to construct a URL for displaying Markdown content from cell `A1`.

### Gzip Compression

GitHub pages only allows [about 8000](https://stackoverflow.com/a/64565317) characters in their URLs. You can squeeze a bit more information by utilizing the `mdz` parameter, which expects base64-encoded gzipped Markdown text.
Using this approach, the basic example above becomes this [link](https://kitware.github.io/markdown-viewer/?mdz=H4sIAAAAAAAA%2F1NW8EjNyclXCM8vyknhCsnILFYAIi0t38Si7JT88jwtLYWS1IoSPQCudMgjKAAAAA%3D%3D):

```
https://kitware.github.io/markdown-viewer/?mdz=H4sIAAAAAAAA%2F1NW8EjNyclXCM8vyknhCsnILFYAIi0t38Si7JT88jwtLYWS1IoSPQCudMgjKAAAAA%3D%3D
```
