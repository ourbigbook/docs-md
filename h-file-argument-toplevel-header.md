# `\H` `file` argument toplevel header

↑ **Parent:** [`\H` `file` argument](h-file-argument.md)

To create a separate file with the [`\H` `file` argument](h-file-argument.md) set on the [toplevel header](the-toplevel-header.md), you must put it under the special [`_file` input directory](file-input-directory.md). For example:
```
_file/path/to/myfile.txt.bigb
```
could contain something like:
```
= myfile.txt
{file}

Description of my amazing file.
```
and it would be associated to the file:
```
path/to/myfile.txt
```

The content of the header `= myfile.txt` is arbitrary, as it can be fully inferred from the file path `_file/path/to/myfile.txt.bigb`. TODO add linting for it. Perhaps we should make adding a header be optional and auto-generate that header instead. But having at least an optional header is good as a way of being able to set header properties like [tags](h-tag-argument.md).

## ↑ Ancestors (6)

1. [`\H` `file` argument](h-file-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`_file` input directory](file-input-directory.md)
