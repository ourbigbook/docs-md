# `id` output format

↑ **Parent:** [`-O --output-format <outformat>`](output-format.md)

This output format is used an intermediate step in [automatic ID from title](automatic-id-from-title.md), that unlike the regular HTML output does not have any tags.

It does not have serious applications to end users. We decided to expose it from the CLI mostly for fun, as it posed no extra work at all as it is treated internally exactly like any other conversion format.

The [`id` output format](id-output-format.md) conversion is very simplistic: it basically just extracts the [`content` argument](content-argument.md) of most macros.

An important exception to that behaviour is the first argument of the [`\x` macro](internal-link.md): see [`\x` `id` output format](x-id-output-format.md).

For example, converting:
```
\i[asdf]
```
with the `id` output format produces simply:
```
asdf
```
instead of the HTML output:
```
<i>asdf</i>
```

This conversion type is useful in situations that users don't expect conversion to produce any HTML tags. For example, you could create a header:
```
= My \i[asdf]
```
and then following the [automatic ID from title](automatic-id-from-title.md) algorithm, that header would have the more commonly desired ID `my-asdf`, and not `my-<i>asdf</i>` or `my-i-asdf-i`.

Similarly, any [macro argument](macro-argument.md) that references an ID undergoes [`id` output format](id-output-format.md) conversion. E.g. the above header could be referenced by:
```
<My \i[asdf]>
```
which is equivalent to:
```
\x[my-asdf]
```

Besides being more intuitive, this conversion also guarantees greater format portability, in case we ever decide to support other output formats besides HTML!

[Macros](macro.md) that don't have a [`content` argument](content-argument.md) are just completely removed, i.e. typically non-textual macros such as [images](image.md). We could put effort in outputting their title argument correctly, but meh, not worth the effort.

The [`id` output format](id-output-format.md) also serves as a good start generalizing OurBigBook to multiple outputs, as this is a simple format.

**Table of contents**

- [`\x` `id` output format](x-id-output-format.md)
- [Unimplemented output formats](unimplemented-output-formats.md)
  - [`latex` output format](latex-output-format.md)

## ↑ Ancestors (4)

1. [`-O --output-format <outformat>`](output-format.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Automatic ID from title](automatic-id-from-title.md)
- [`Id` output format](id-output-format.md)
