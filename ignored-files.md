# Ignored files

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

The following files are ignored from conversion:
- [`ignore`](ourbigbook-json/ignore.md) patterns
- gitignored files: [Section "Ignore from `.gitignore`"](ignore-from-gitignore.md)
- a few hardcoded basenames, such as `.git` and [the `_out` directory](the-out-directory.md), see `DEFAULT_IGNORE_BASENAMES` in [ourbigbook](ourbigbook)
Note that this applies even if you try to convert a single ignored file such as:
```
ourbigbook ignored.bigb
```
We are strict about this in order to prevent accidentally polluting the database with temporary data.

**Table of contents**

- [Ignore from `.gitignore`](ignore-from-gitignore.md)

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)
