<h1 id="ourbigbook-json/web/linkfromstaticheadermetatoweb"><code>linkFromStaticHeaderMetaToWeb</code></h1>

↑ **Parent:** [`Web`](../web.md)

<a id="ourbigbook-json/web/_3950"></a>
Type: boolean. Default: `false`.

<a id="ourbigbook-json/web/_3951"></a>
If `true`, adds a link under the metadata section of every header of a [OurBigBook CLI](../../ourbigbook-cli.md) static website pointing to the corresponding article on [OurBigBook.com](../../ourbigbook-com.md), or another [OurBigBook Web](../../ourbigbook-web.md) instance specified by the [`host`](host.md) option.

<a id="ourbigbook-json/web/_3952"></a>
It also sends you to Heaven for supporting the project.

<a id="ourbigbook-json/web/_3953"></a>
This option requires [`username`](username.md) to be set.

<a id="ourbigbook-json/web/_3954"></a>
For example, if you set:<a id="ourbigbook-json/web/_3955"></a>

```
"web": {
  "username": "myusername",
  "linkFromStaticHeaderMetaToWeb": true
}
```
then in the rendering of a index.bigb:<a id="ourbigbook-json/web/_3956"></a>

```
= Index

== My h2
{scope}

=== My h2 2
{scope}
```
those headers would have a metadata entry pointing respectively to:<a id="ourbigbook-json/web/_3957"></a>

<a id="ourbigbook-json/web/_3958"></a>
- `https://ourbigbook.com/myusername`
<a id="ourbigbook-json/web/_3959"></a>
- `https://ourbigbook.com/myusername/my-h2`
<a id="ourbigbook-json/web/_3960"></a>
- `https://ourbigbook.com/myusername/my-h2/my-h2-2`

<a id="ourbigbook-json/web/_3961"></a>
In order for such links not to be broken, you should always first do a [Web upload](../../web.md) to ensure that the articles are present on [OurBigBook.com](../../ourbigbook-com.md).

<a id="ourbigbook-json/web/_3962"></a>
Previously named `linkFromHeaderMeta`.

## ↑ Ancestors (4)

1. [`Web`](../web.md)
2. [`Ourbigbook.json`](../../ourbigbook-json.md)
3. [OurBigBook CLI](../../ourbigbook-cli.md)
4. [OurBigBook Project](../../split.md)

## ← Incoming links (3)

- [`Host`](host.md)
- [`HostCapitalized`](hostcapitalized.md)
- [`Username`](username.md)
