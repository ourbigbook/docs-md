<h1 id="ourbigbook-json/web/linkfromstaticheadermetatoweb"><code>linkFromStaticHeaderMetaToWeb</code></h1>

↑ **Parent:** [`Web`](../web.md)

Type: boolean. Default: `false`.

If `true`, adds a link under the metadata section of every header of a [OurBigBook CLI](../../ourbigbook-cli.md) static website pointing to the corresponding article on [OurBigBook.com](../../ourbigbook-com.md), or another [OurBigBook Web](../../ourbigbook-web.md) instance specified by the [`host`](host.md) option.

It also sends you to Heaven for supporting the project.

This option requires [`username`](username.md) to be set.

For example, if you set:
```
"web": {
  "username": "myusername",
  "linkFromStaticHeaderMetaToWeb": true
}
```
then in the rendering of a index.bigb:
```
= Index

== My h2
{scope}

=== My h2 2
{scope}
```
those headers would have a metadata entry pointing respectively to:
- `https://ourbigbook.com/myusername`
- `https://ourbigbook.com/myusername/my-h2`
- `https://ourbigbook.com/myusername/my-h2/my-h2-2`

In order for such links not to be broken, you should always first do a [Web upload](../../web.md) to ensure that the articles are present on [OurBigBook.com](../../ourbigbook-com.md).

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
