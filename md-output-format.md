# `md` output format

↑ **Parent:** [`-O --output-format <outformat>`](output-format.md)

Exports editable Markdown with OurBigBook extensions, rather than GitHub deployment Markdown:
```
ourbigbook -O md index.bigb
```

The output is written to `_out/md/index.md`. Headers, ordinary paragraphs, emphasis, code, unordered lists and block images prefer Markdown shorthand. Magic cross-references use `[[target]]` or `[[target|label]]`, and labelled external links use `https://example.com[label]`. Native macros and arguments remain available where shorthand cannot preserve meaning. Includes remain includes rather than being expanded into the exported source. Assets are copied alongside the Markdown with their relative paths preserved; original markup files are not copied into `-/raw`. The goal is semantic AST equivalence after reading the Markdown back, including paragraph nesting, IDs and scope. Regression tests compare both ASTs and rendered HTML. Explicit paragraph macros remain necessary for empty paragraphs and certain nested or whitespace-sensitive paragraphs. This is not yet an automatic in-place repository migration: verify the exported sources, includes, configuration and media paths before replacing existing files.

## ↑ Ancestors (4)

1. [`-O --output-format <outformat>`](output-format.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)
