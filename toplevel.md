<h1 id="toplevel">The <code>\Toplevel</code> implicit macro</h1>

↑ **Parent:** [Internals API](internals-api.md)

Every OurBigBook document is implicitly put inside a `\Toplevel` document and:
- any optionally given arguments at the very beginning of the document will be treated as arguments of the `\Toplevel` macro
- anything else will be put inside the [`content` argument](content-argument.md) of the `\Toplevel` macro

E.g., a OurBigBook document that contains:
```
{title=My favorite title}

And now, some content!
```

is morally equivalent to:
```
\Toplevel{title=My favorite title}
[
And now, some content!
]
```
In terms of HTML, the `\Toplevel` element corresponds to the `<html>`, `<head>`, `<header>` and `<footer>` elements of a document.

Trying to use the `\Toplevel` macro explicitly in a document leads to an error.

## ↑ Ancestors (3)

1. [Internals API](internals-api.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Code block](code-block.md)
- [Image](image.md)
- [List](list.md)
- [Table](table.md)
