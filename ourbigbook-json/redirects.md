<h1 id="ourbigbook-json/redirects"><code>redirects</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3919"></a>
Generate custom redirects.

<a id="ourbigbook-json/_3920"></a>
For example:<a id="ourbigbook-json/_3921"></a>

```
"redirects": [
  ["cirodown", "ourbigbook"]
],
```
produces a file in the output called `cirodown.html` that redirects to `ourbigbook.html`.

<a id="ourbigbook-json/_3922"></a>
Absolute URLs are also accepted, e.g.:<a id="ourbigbook-json/_3923"></a>

```
"redirects": [
  ["ourbigbook", "https://docs.ourbigbook.com"]
],
```
produces a file in the output called `ourbigbook.html` that redirects to `https://docs.ourbigbook.com`.

<a id="ourbigbook-json/_3924"></a>
When dealing with regular [headers](../header.md), you generally don't want to use this option and instead use the [`\H` `synonym` argument](../h-synonym-argument.md), which already creates the redirection for you.

<a id="ourbigbook-json/_3925"></a>
This JSON option can be useful however for dealing with things that are outside of your OurBigBook project.

<a id="ourbigbook-json/_3926"></a>
For example, at one point, this project renamed the repository [https://github.com/cirosantilli/cirodown](https://github.com/cirosantilli/cirodown) to [https://github.com/ourbigbook/ourbigbook](https://github.com/ourbigbook/ourbigbook).

<a id="ourbigbook-json/_3927"></a>
Unfortunately, GitHub Pages does not generate redirects like github.com itself.

<a id="ourbigbook-json/_3928"></a>
So in this case, we've added to the [`ourbigbook.json`](../ourbigbook-json.md) of the toplevel user repository [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) the lines:<a id="ourbigbook-json/_3929"></a>

```
"redirects": [
  ["cirodown", "ourbigbook"]
],
```
which produces a file in the output called `cirodown.html` that redirects to `ourbigbook.html`.

<a id="ourbigbook-json/_3930"></a>
In this case, `cirodown` and `ourbigbook` don't have to be any regular IDs present in the database, those strings are just used directly.

<a id="ourbigbook-json/_3931"></a>
TODO ideally we should check for conflicts with regular output from split headers IDs or their synonyms. But lazy.

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)
