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
  - [Not index md](not-index-md.md)
    - [Not index md h2 1](not-index-md.md#not-index-md-h2-1)
    - [Not index md h2 2](not-index-md.md#not-index-md-h2-2)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
