# stdin conversion

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

Convert a `.bigb` file from stdin to HTML and output the contents of `<body>` to stdout:
```
printf 'ab\ncd\n' | ourbigbook --body-only
```

Stdin converion is a bit different from conversion from a file in that it ignores the [`ourbigbook.json`](ourbigbook-json.md) and any other setting files present in the current directory or its ancestors. Also, it does not produce any changes to the [ID database](cross-file-internal-link-internals.md). In other words, a conversion from stdin is always treated as if it were outside of any project, and therefore should always produce the same results regardless of the current working directory.

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)
