# `\x` `id` output format

↑ **Parent:** [`Id` output format](id-output-format.md)

`\x` uses `href` if the content is not given explicitly.

Previously, if `\x` didn't have a content, we were actually rendering the `\x` to calculate the ID. But then we noticed that doing so would require another parse pass, so we just went for this simpler approach. This is closely linked to [`\x` within `title` restrictions](x-within-title-restrictions.md).

For example in:

```
= Animal

\x[image-i-like-dog]

\Image[dog.jpg]
{title=I \i[like] \x[dog]}

== Dog hacked
{id=dog}
```

If you wanted `image-i-like-dog-hacked` instead, you would need to explicitly give it as in:
```
= Animal

\x[image-i-like-dog-hacked]

\Image[dog.jpg]
{title=I like \x[dog][dog hacked]}

== Dog hacked
{id=dog}
```

For similar reasons as the above, `{p}` inflection with the [`\x` `p` argument](x-p-argument.md) is not considered either, e.g. you would have:
```
= Animal

\x[image-i-like-dog]

\Image[dog.jpg]
{title=I like \x[dog]{p}}

== Dog
```
and not:
```
\x[image-i-like-dogs]
```

This can however be worked around with the [`\x` `magic` argument](x-magic-argument.md) as in;
```
= Animal

\x[image-i-like-dogs]

\Image[dog.jpg]
{title=I like <dogs>}

== Dog
```

## ↑ Ancestors (5)

1. [`Id` output format](id-output-format.md)
2. [`-O --output-format <outformat>`](output-format.md)
3. [OurBigBook CLI options](ourbigbook-cli-options.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`Id` output format](id-output-format.md)
- [`\x` within `title` restrictions](x-within-title-restrictions.md)
