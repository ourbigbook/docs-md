<h1 id="ourbigbook-json/h/numbered"><code>numbered</code></h1>

↑ **Parent:** [`H`](../h.md)

Sets the default [`\H` `numbered` argument](../../h-numbered-argument.md) argument of the toplevel headers of each source file.

Note that since the option is inherited by descendants, this can also affect the rendering of ancestors.

[https://github.com/ourbigbook/ourbigbook/issues/188](https://github.com/ourbigbook/ourbigbook/issues/188) contains a proposal to instead inherit this property across [includes](../../include.md).

If you set this ourbigbook.json option:
```
{
  "h": {
    "numbered": true
  }
}
```
it is possible to override it for a specific file with and explicit `=0` [`\H` `numbered` argument](../../h-numbered-argument.md):
```
= Not numbered exception
{numbered=0}

== Child also inherits not numbered
```

Make every link to something that is not on the current page open on a new tab instead of the current one, i.e. add `target="_blank"` to such links.

## ↑ Ancestors (4)

1. [`H`](../h.md)
2. [`Ourbigbook.json`](../../ourbigbook-json.md)
3. [OurBigBook CLI](../../ourbigbook-cli.md)
4. [OurBigBook Project](../../split.md)

## ← Incoming links (1)

- [`SplitDefault`](splitdefault.md)
