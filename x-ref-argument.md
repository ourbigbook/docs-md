# `\x` `ref` argument

↑ **Parent:** [`\x` arguments](x-arguments.md)

The `ref` argument of `\x` marks the link as reference, e.g.:
```
Trump said this and that.\x[donald-trump-access-hollywood-tape]{ref}

= Donald Trump Access Hollywood tape
```
renders something like:
```
Trump said this and that.<a href="donald-trump-access-hollywood-tape">*</a>
```

This could currently be replicated without `ref` by just using:
```
Trump said this and that.\x[donald-trump-access-hollywood-tape][*]
```
but later on we might add more precise reference fields like the page of a book or date fetched as Wikipedia supports.

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/137](https://github.com/ourbigbook/ourbigbook/issues/137)

## ↑ Ancestors (5)

1. [`\x` arguments](x-arguments.md)
2. [Internal link](internal-link.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\a` `ref` argument](a-ref-argument.md)
