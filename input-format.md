<h1 id="input-format"><code>-I --input-format &lt;inputformat&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Selects the input format.

Supported values:
- `bigb`: the default an recommended format
- `md`, see: [`--input-format md`](input-format-md.md)

The input format is automatically selected from the file extension, e.g. `.md` or `.markdown` input files. For input from standard input, it can be selected explicitly e.g. with:
```
printf '# Hello' | ourbigbook -I markdown -O bigb --stdout
```

Directory conversion remains BigB-only unless `-I markdown` is given, so that Markdown documentation files such as `README.md` are not compiled unexpectedly.

**Table of contents**

- [`--input-format md`](input-format-md.md)
  - [Markdown example](markdown-example.md)
    - [OurBigBook Markdown extensions](markdown-example.md#ourbigbook-markdown-extensions)
      - [Markdown example child](markdown-example-child.md)
      - [OurBigBook Markdown shorthand extensions](markdown-example.md#ourbigbook-markdown-shorthand-extensions)
        - [OurBigBook Markdown wikilinks](markdown-example.md#ourbigbook-markdown-wikilinks)
      - [OurBigBook Markdown extensions h3](markdown-example.md#ourbigbook-markdown-extensions-h3)
        - [OurBigBook Markdown extensions h4](markdown-example.md#ourbigbook-markdown-extensions-h4)
          - [OurBigBook Markdown extensions h5](markdown-example.md#ourbigbook-markdown-extensions-h5)
            - [OurBigBook Markdown extensions h6](markdown-example.md#ourbigbook-markdown-extensions-h6)
              - [OurBigBook Markdown extensions h7](markdown-example.md#ourbigbook-markdown-extensions-h7)
                - [OurBigBook Markdown extensions h8](markdown-example.md#ourbigbook-markdown-extensions-h8)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
