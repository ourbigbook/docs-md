<h1 id="ourbigbook-json/redirects"><code>redirects</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

Generate custom redirects.

For example:
```
"redirects": [
  ["cirodown", "ourbigbook"]
],
```
produces a file in the output called `cirodown.html` that redirects to `ourbigbook.html`.

Absolute URLs are also accepted, e.g.:
```
"redirects": [
  ["ourbigbook", "https://docs.ourbigbook.com"]
],
```
produces a file in the output called `ourbigbook.html` that redirects to `https://docs.ourbigbook.com`.

When dealing with regular [headers](../header.md), you generally don't want to use this option and instead use the [`\H` `synonym` argument](../h-synonym-argument.md), which already creates the redirection for you.

This JSON option can be useful however for dealing with things that are outside of your OurBigBook project.

For example, at one point, this project renamed the repository [https://github.com/cirosantilli/cirodown](https://github.com/cirosantilli/cirodown) to [https://github.com/ourbigbook/ourbigbook](https://github.com/ourbigbook/ourbigbook).

Unfortunately, GitHub Pages does not generate redirects like github.com itself.

So in this case, we've added to the [`ourbigbook.json`](../ourbigbook-json.md) of the toplevel user repository [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) the lines:
```
"redirects": [
  ["cirodown", "ourbigbook"]
],
```
which produces a file in the output called `cirodown.html` that redirects to `ourbigbook.html`.

In this case, `cirodown` and `ourbigbook` don't have to be any regular IDs present in the database, those strings are just used directly.

TODO ideally we should check for conflicts with regular output from split headers IDs or their synonyms. But lazy.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)
