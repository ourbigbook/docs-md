# `github-md` output format

↑ **Parent:** [`-O --output-format <outformat>`](output-format.md)

Outputs GitHub deployment Markdown to a `.md` file. This is distinct from the editable `md` input format with OurBigBook extensions.

The portable common subset of OurBigBook headers, paragraphs, emphasis, links, images, code, quotes, lists, horizontal rules, mathematics and tables is converted to the closest Markdown construct.

For example:
```
ourbigbook -O github-md index.bigb
```

This output targets GitHub's renderer, including its heading anchors, generated navigation and size limits. It is a rendered deployment format, not a lossless source conversion. `--publish-target github-md` selects it automatically.

## ↑ Ancestors (4)

1. [`-O --output-format <outformat>`](output-format.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`Adoc` output format](adoc-output-format.md)
- [`--input-format md`](input-format-md.md)
