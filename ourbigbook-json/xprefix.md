<h1 id="ourbigbook-json/xprefix"><code>xPrefix</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3965"></a>
If given, prepend the given string to every single [internal cross file internal link](../cross-file-internal-link.md) output.

<a id="ourbigbook-json/_3966"></a>
The initial application of this option was to [Section "Redirect from a static website to a dynamic website"](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md).

<a id="ourbigbook-json/_3967"></a>
E.g. suppose that you previously had at `myoldsite.com` you had:

<a id="ourbigbook-json/_3968"></a>
animal.bigb<a id="ourbigbook-json/_3969"></a>

```
= Animal

<Dogs> don't eat <bananas>.

== Dog
```

<a id="ourbigbook-json/_3970"></a>
plant.bigb<a id="ourbigbook-json/_3971"></a>

```
= Plant

== Banana
```
Originally that would render as:<a id="ourbigbook-json/_3972"></a>

```
<a href="#dog">Dogs</a> don't eat <a href="plant#banana">bananas</a>.
```

<a id="ourbigbook-json/_3973"></a>
But then if you set in `ourbigbook.json`:<a id="ourbigbook-json/_3974"></a>

```
{
  "xPrefix": "https://mynewsite.com/"
}
```
it will instead render as:<a id="ourbigbook-json/_3975"></a>

```
<a href="#dog">Dogs</a> don't eat <a href="https://mynewsite.com/plant#banana">bananas</a>.
```
where:<a id="ourbigbook-json/_3976"></a>

<a id="ourbigbook-json/_3977"></a>
- dogs: untouched as it links to the same page as the current one
<a id="ourbigbook-json/_3978"></a>
- bananas: the prefix is added, as it is on another page

<a id="ourbigbook-json/_3979"></a>
[Scopes](../h-scope-argument.md) are automatically resolved so that they will also be present in the target. E.g. in:

<a id="ourbigbook-json/_3980"></a>
subdir/notindex.bigb<a id="ourbigbook-json/_3981"></a>

```
<notindex2>
```

<a id="ourbigbook-json/_3982"></a>
subdir/notindex2.bigb<a id="ourbigbook-json/_3983"></a>

```
= Notindex2
```

<a id="ourbigbook-json/_3984"></a>
we get on `subdir/notindex.html`:<a id="ourbigbook-json/_3985"></a>

```
<a href="https://mynewsite.com/subdir/notindex2.html">
```
and not:<a id="ourbigbook-json/_3986"></a>

```
<a href="https://mynewsite.com/notindex2.html">
```

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Make all links of a static website point to another deployment of the website](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md)
