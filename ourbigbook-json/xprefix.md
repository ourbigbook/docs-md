<h1 id="ourbigbook-json/xprefix"><code>xPrefix</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

If given, prepend the given string to every single [internal cross file internal link](../cross-file-internal-link.md) output.

The initial application of this option was to [Section "Redirect from a static website to a dynamic website"](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md).

E.g. suppose that you previously had at `myoldsite.com` you had:

animal.bigb
```
= Animal

<Dogs> don't eat <bananas>.

== Dog
```

plant.bigb
```
= Plant

== Banana
```
Originally that would render as:
```
<a href="#dog">Dogs</a> don't eat <a href="plant#banana">bananas</a>.
```

But then if you set in `ourbigbook.json`:
```
{
  "xPrefix": "https://mynewsite.com/"
}
```
it will instead render as:
```
<a href="#dog">Dogs</a> don't eat <a href="https://mynewsite.com/plant#banana">bananas</a>.
```
where:
- dogs: untouched as it links to the same page as the current one
- bananas: the prefix is added, as it is on another page

[Scopes](../h-scope-argument.md) are automatically resolved so that they will also be present in the target. E.g. in:

subdir/notindex.bigb
```
<notindex2>
```

subdir/notindex2.bigb
```
= Notindex2
```

we get on `subdir/notindex.html`:
```
<a href="https://mynewsite.com/subdir/notindex2.html">
```
and not:
```
<a href="https://mynewsite.com/notindex2.html">
```

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Make all links of a static website point to another deployment of the website](../make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md)
