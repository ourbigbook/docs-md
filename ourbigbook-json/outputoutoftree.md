<h1 id="ourbigbook-json/outputoutoftree"><code>outputOutOfTree</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

Default: `true`

If `true` place the HTML output under [the `_out` directory](../the-out-directory.md) at `_out/html`.

For example with:
```
{
  "outputOutOfTree": false
}
```
then
```
ourbigbook hello.bigb
```
would be place its output under:
```
hello.html
```
instead of `_out/html/hello.html`.

Advantages of `outputOutOfTree=true`:
- the source tree becomes cleaner, especially when using [`-S`, `--split-headers`](../split-headers.md) which can produce hundreds of output files from a single input file
- if you want to track several `.html` source files in-tree, you don't need to add an exception to each of of them on the `.gitignore` as:
  ```
  *.html
  !/ourbigbook.liquid.html
  ```
Disadvantages:
- you have to type more to open each output file on the terminal

This option is always forced to `false` when [`--outdir <outdir>`](../outdir.md) is given.

Implemented at: [https://github.com/ourbigbook/ourbigbook/issues/163](https://github.com/ourbigbook/ourbigbook/issues/163)

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Run OurBigBook master](../run-ourbigbook-master.md)
