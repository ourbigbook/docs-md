<h1 id="input-format"><code>-I --input-format &lt;inputformat&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Selects the CLI input frontend. Supported values are `bigb` (the default) and `markdown`. Markdown is automatically selected for `.md` and `.markdown` input files, and can be selected explicitly for standard input:
```
printf '# Hello' | ourbigbook -I markdown -O bigb --stdout
```

Directory conversion remains BigB-only unless `-I markdown` is given, so that Markdown documentation files such as `README.md` are not compiled unexpectedly.

The Markdown frontend uses Marked to tokenize Markdown, converts those tokens to the OurBigBook AST through canonical OurBigBook source, and then uses the normal ID, validation and rendering pipeline. This is currently CLI-only.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
