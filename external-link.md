# External link

↑ **Parent:** [`\a` `external` argument](a-external-argument.md)

An external link is a link that points to a resource that is not present in the current OurBigBook project sources. A typical external link is something like:
```
This is great website: https://cirosantilli.com
```
which renders as:



> This is great website: [https://cirosantilli.com](https://cirosantilli.com)

which points to an absolute URL.

[Internal path links](external-link.md) are links that point to files present inside the current project. For example, in computer programming tutorials we will often want to refer to source files in the current directory. So from our `index.bigb`, we could want to write something like:
```
Have a look at this amazing source file: \a[index.js].
```
which renders as:



> Have a look at this amazing source file: [index.js](index.js).

and here `\a[ourbigbook]` is a internal link. These should not to be confused with [internal links](internal-link.md), which may point not only to files, but to any [ID](element-id.md), e.g. of headers inside a OurBigBook file.

OurBigBook considers a link external by default if it does not have a [URL with protocol](url-with-protocol.md).

Therefore, the following links are external by default:
- `http://cirosantilli.com`
- `https://cirosantilli.com`
- `file:///etc/fstab`
- `ftp://cirosantilli.com`
and the following are internal by default:
- `index.js`
- `../index.js`
- `path/to/index.js`
- `/path/to/index.js`. Note that paths starting with `/` refer to the root of the [OurBigBook CLI](ourbigbook-cli.md) deployment, not the root of the domain, see: [link to the domain root path](link-to-the-domain-root-path.md).
- `//example.com/path/to/index.js`

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/87](https://github.com/ourbigbook/ourbigbook/issues/87) as `relative`, and subsequently modified to the more accurate/useful `external`.

**Table of contents**

- [Internal path links are smart](internal-path-links-are-smart.md)

## ↑ Ancestors (6)

1. [`\a` `external` argument](a-external-argument.md)
2. [`\a` argument](a-argument.md)
3. [Link](link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`\a` `external` argument](a-external-argument.md)
