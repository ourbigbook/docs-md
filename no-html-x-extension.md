<h1 id="no-html-x-extension"><code>--no-html-x-extension</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

If not given, [internal links](internal-link.md) render with the `.html` extension as in:
```
<a href=not-index.html#h2-in-not-the-index>
```

This way, those links will work when rendering locally to `.html` files which is the default behaviour of:
```
ourbigbook .
```

If given however, the links render without the `.html` as in:
```
<a href=not-index#h2-in-not-the-index>
```
which is what is needed for servers such as GitHub Pages, which automatically remove the `.html` extension from paths.

This option is automatically implied when [publishing to targets that remove the `.html` extension such as GitHub pages](publish-target-github-pages.md).

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`HtmlXExtension`](ourbigbook-json/htmlxextension.md)
