# Internal link targets in split headers

↑ **Parent:** [`-S`, `--split-headers`](split-headers.md)

By default, all [internal links](internal-link.md) point to the non-split version of headers, including those found in split headers.

The rationale for this is that it gives readers the most context around the header by simply scrolling.

For example, considering the example document at [`-S`, `--split-headers`](split-headers.md), [internal links](internal-link.md) such as `\x[h1-1]` would point:
- from the non-split `hello.html` to the section in the current non-split file `#h1-1`
- from split `hello-split.html` to the same section in non-split file with `hello.html#h1-1`
The same applies to [cross file internal links](cross-file-internal-link.md) when there are multiple input files.

In order to make the split version be the default for some headers, you can use the [`\H` `splitDefault` argument](h-splitdefault-argument.md).

This is something that we might consider changing with some option, e.g. keeping the split headers more self contained. But for now, the general feeling is that going to nosplit by default is the best default.

## ↑ Ancestors (4)

1. [`-S`, `--split-headers`](split-headers.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
