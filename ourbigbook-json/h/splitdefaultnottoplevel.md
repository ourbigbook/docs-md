<h1 id="ourbigbook-json/h/splitdefaultnottoplevel"><code>splitDefaultNotToplevel</code></h1>

↑ **Parent:** [`H`](../h.md)

<a id="ourbigbook-json/h/_3820"></a>
If given, the toplevel output of each input source is always non-split, and a split version is not generated at all.

<a id="ourbigbook-json/h/_3821"></a>
This of course overrides the [`\H` `splitDefault` argument](../../h-splitdefault-argument.md) for toplevel headers, making any links go to the non split version, as we won't have a split version at all in this case.

<a id="ourbigbook-json/h/_3822"></a>
E.g.:

<a id="ourbigbook-json/h/_3823"></a>
ourbigbook.json<a id="ourbigbook-json/h/_3824"></a>

```
{
  "h": {
    "splitDefault": true,
    "splitDefaultNoToplevel": true,
  }
}
```

<a id="ourbigbook-json/h/_3825"></a>
my-first-header.bigb<a id="ourbigbook-json/h/_3826"></a>

```
= My first header

== My second header
```

<a id="ourbigbook-json/h/_3827"></a>
When converted with:<a id="ourbigbook-json/h/_3828"></a>

```
ourbigbook --split-headers my-first-header.bigb
```
would lead only to two output files:<a id="ourbigbook-json/h/_3829"></a>

<a id="ourbigbook-json/h/_3830"></a>
- my-first-header: not split
<a id="ourbigbook-json/h/_3831"></a>
- my-second-header: split

<a id="ourbigbook-json/h/_3832"></a>
Without `splitDefaultNoToplevel` we would instead have:<a id="ourbigbook-json/h/_3833"></a>

<a id="ourbigbook-json/h/_3834"></a>
- my-first-header: split
<a id="ourbigbook-json/h/_3835"></a>
- my-first-header-nosplit: not split
<a id="ourbigbook-json/h/_3836"></a>
- my-second-header: split

<a id="ourbigbook-json/h/_3837"></a>
The initial use case for this was in [OurBigBook Web](../../ourbigbook-web.md). If we didn't do this, then there would be two versions of every article at the toplevel of a file: split and nosplit.

<a id="ourbigbook-json/h/_3838"></a>
This would be confusing for users, who would e.g. see two new articles on the article index every time they create a new one.

<a id="ourbigbook-json/h/_3839"></a>
It would also mean that metadata such as comments would be visible in two separate locations.

<a id="ourbigbook-json/h/_3840"></a>
So instead of filtering the duplicate articles on every index, we just don't generate them in the first place.

## ↑ Ancestors (4)

1. [`H`](../h.md)
2. [`Ourbigbook.json`](../../ourbigbook-json.md)
3. [OurBigBook CLI](../../ourbigbook-cli.md)
4. [OurBigBook Project](../../split.md)
