<h1 id="ourbigbook-json/h/splitdefaultnottoplevel"><code>splitDefaultNotToplevel</code></h1>

↑ **Parent:** [`H`](../h.md)

If given, the toplevel output of each input source is always non-split, and a split version is not generated at all.

This of course overrides the [`\H` `splitDefault` argument](../../h-splitdefault-argument.md) for toplevel headers, making any links go to the non split version, as we won't have a split version at all in this case.

E.g.:

ourbigbook.json
```
{
  "h": {
    "splitDefault": true,
    "splitDefaultNoToplevel": true,
  }
}
```

my-first-header.bigb
```
= My first header

== My second header
```

When converted with:
```
ourbigbook --split-headers my-first-header.bigb
```
would lead only to two output files:
- my-first-header: not split
- my-second-header: split

Without `splitDefaultNoToplevel` we would instead have:
- my-first-header: split
- my-first-header-nosplit: not split
- my-second-header: split

The initial use case for this was in [OurBigBook Web](../../ourbigbook-web.md). If we didn't do this, then there would be two versions of every article at the toplevel of a file: split and nosplit.

This would be confusing for users, who would e.g. see two new articles on the article index every time they create a new one.

It would also mean that metadata such as comments would be visible in two separate locations.

So instead of filtering the duplicate articles on every index, we just don't generate them in the first place.

## ↑ Ancestors (4)

1. [`H`](../h.md)
2. [`Ourbigbook.json`](../../ourbigbook-json.md)
3. [OurBigBook CLI](../../ourbigbook-cli.md)
4. [OurBigBook Project](../../split.md)
