# `bigb` output format

↑ **Parent:** [`-O --output-format <outformat>`](output-format.md)

Outputs as [OurBigBook Markup](ourbigbook-markup.md), i.e. the same format as the input itself!

While using `-O bigb` is not a common use case, the existence of this format has the following applications:
- automatic source code formatting e.g. with [`--format-source`](format-source.md). The recommended format, including several edge cases, can be seen in the test file [test_bigb_output.bigb](test_bigb_output.bigb), which should be left unchanged by a `bigb` conversion.
- manipulating source code on [OurBigBook Web](ourbigbook-web.md) to allow editing either individual sections separatelly, or multiple sections at once
- this could be adapted to allows us to migrate updates with breaking changes to the source code more easily. Alternatively on [OurBigBook Web](ourbigbook-web.md), we might just start storing the [AST](abstract-syntax-tree.md) instead of source, and just rendering the source whenever users want to edit it.

Can be tested interactively with:
```
ourbigbook --no-db -O bigb --stdout --log=ast-simple test_bigb_output.bigb
```

One important property of the `bigb` conversion is that is must not alter the [AST](abstract-syntax-tree.md), and therefore neither the final output, in any way.

One good test is:
```
ourbigbook index.bigb &&
mv _out/html/index.html _out/html/old.html &&
ourbigbook --format-source index.bigb  &&
ourbigbook index.bigb &&
diff -u _out/html/old.html _out/html/index.html
```

This was tracked at: [https://github.com/ourbigbook/ourbigbook/issues/83](https://github.com/ourbigbook/ourbigbook/issues/83)

## 🏷️ Tagged (1)

- [Ordered list lost when rendering to bigb output format](todo/ordered-list-lost-when-rendering-to-bigb-output-format.md)

## ↑ Ancestors (4)

1. [`-O --output-format <outformat>`](output-format.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--format-source`](format-source.md)
