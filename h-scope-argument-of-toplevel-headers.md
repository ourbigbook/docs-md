# `\H` `scope` argument of toplevel headers

↑ **Parent:** [`\H` `scope` argument](h-scope-argument.md)

When [the toplevel header](the-toplevel-header.md) is given the `scope` property OurBigBook automatically uses the file path for the scope and heaves fragments untouched.

For example, suppose that file `full-and-unique-experiment-name` contains:
```
= Full and unique experiment name
{scope}

== Introduction

== Materials
```

In this case, multi-file output will generate a file called `full-and-unique-experiment-name.html`, and the URL of the subsections will be just:
- `full-and-unique-experiment-name.html#introduction`
- `full-and-unique-experiment-name.html#materials`
instead of
- `full-and-unique-experiment-name.html#full-and-unique-experiment-name/introduction`
- `full-and-unique-experiment-name.html#full-and-unique-experiment-name/materials`

Some quick interactive cross file link tests:
- [not the index with scope](not-index-with-scope-split.md)
- [h2](not-index-with-scope/h2.md)
- [Figure "My image"](not-index-with-scope/h2.md#image-my-image)

## ↑ Ancestors (6)

1. [`\H` `scope` argument](h-scope-argument.md)
2. [`\H` arguments](h-arguments.md)
3. [Header](header.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
