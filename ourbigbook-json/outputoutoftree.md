<h1 id="ourbigbook-json/outputoutoftree"><code>outputOutOfTree</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3886"></a>
Default: `true`

<a id="ourbigbook-json/_3887"></a>
If `true` place the HTML output under [the `_out` directory](../the-out-directory.md) at `_out/html`.

<a id="ourbigbook-json/_3888"></a>
For example with:<a id="ourbigbook-json/_3889"></a>

```
{
  "outputOutOfTree": false
}
```
then<a id="ourbigbook-json/_3890"></a>

```
ourbigbook hello.bigb
```
would be place its output under:<a id="ourbigbook-json/_3891"></a>

```
hello.html
```
instead of `_out/html/hello.html`.

<a id="ourbigbook-json/_3892"></a>
Advantages of `outputOutOfTree=true`:<a id="ourbigbook-json/_3893"></a>

<a id="ourbigbook-json/_3894"></a>
- the source tree becomes cleaner, especially when using [`-S`, `--split-headers`](../split-headers.md) which can produce hundreds of output files from a single input file
<a id="ourbigbook-json/_3895"></a>
- if you want to track several `.html` source files in-tree, you don't need to add an exception to each of of them on the `.gitignore` as:<a id="ourbigbook-json/_3896"></a>

  ```
  *.html
  !/ourbigbook.liquid.html
  ```
Disadvantages:<a id="ourbigbook-json/_3897"></a>

<a id="ourbigbook-json/_3898"></a>
- you have to type more to open each output file on the terminal

<a id="ourbigbook-json/_3899"></a>
This option is always forced to `false` when [`--outdir <outdir>`](../outdir.md) is given.

<a id="ourbigbook-json/_3900"></a>
Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/163](https://github.com/ourbigbook/ourbigbook/issues/163)

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Run OurBigBook master](../run-ourbigbook-master.md)
