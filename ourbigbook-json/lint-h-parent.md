<h1 id="ourbigbook-json/lint-h-parent"><code>lint</code> <code>h-parent</code></h1>

↑ **Parent:** [`Lint`](lint.md)

<a id="ourbigbook-json/_3802"></a>
Possible values:<a id="ourbigbook-json/_3803"></a>

<a id="ourbigbook-json/_3804"></a>
- `parent`: forces headers to use [`\H` `parent` argument](../h-parent-argument.md) to specify their level
<a id="ourbigbook-json/_3805"></a>
- `number`: forces headers to not use [`\H` `parent` argument](../h-parent-argument.md) to specify their level, i.e. to use a number or a number of `=`

<a id="ourbigbook-json/_3806"></a>
You should basically always set either one of those on any serious project. Forgetting a `parent=` in a project that uses `parent=` everywhere else is a common cause of build bugs, and can be hard to debug without this type of linting enabled.

## ↑ Ancestors (4)

1. [`Lint`](lint.md)
2. [`Ourbigbook.json`](../ourbigbook-json.md)
3. [OurBigBook CLI](../ourbigbook-cli.md)
4. [OurBigBook Project](../split.md)
