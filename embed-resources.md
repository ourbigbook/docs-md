<h1 id="embed-resources"><code>--embed-resources</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Embed as many external resources such as images and CSS as possible into the HTML output files, rather than linking to external resources.

For example, when converting a simple document to HTML:

index.bigb
```
= Index

My paragraph.
```

with:
```
ourbigbook index.bigb
```
the output contains references to where OurBigBook is installed in our local filesystem:
```
<style>
@import "/home/ciro/bak/git/ourbigbook/_obb/ourbigbook.css";
</style>
<script src="/home/ciro/bak/git/ourbigbook/_obb/ourbigbook_runtime.js"></script>
```
The advantage of this is that we don't have to duplicate this for every single file. But if you are giving this file to someone else, they would likely not have those files at those exact locations, which would break the HTML page.

With `--embed-resources`, the output contains instead something like:
```
<style>/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */html{ [[ ... A LOT MORE CSS ... ]]</style>
<script>/*! For license information please see ourbigbook_runtime.js.LICENSE.txt */ !function(t,e){"object"==typeof exports&&"object"==typeof module?module.exports=e() [[ ... A LOT MORE JAVASCRIPT ... ]]</script>
```
This way, all the required CSS and JavaScript will be present in the HTML file itself, and so readers will be able to view the file correctly without needing to install any missing dependencies.

The use case for this option is to produce a single HTML file for an entire build that is fully self contained, and can therefore be given to consumers and viewed offline, much like a PDF.

Examples of embeddings done:
- CSS and JavaScript are copy pasted in place into the HTML.

  The default built-in CSS and JavaScript files used by OurBigBook (e.g. the KaTeX CSS [used for mathematics](mathematics.md)) are currently all automatically downloaded as NPM package dependencies to ourbigbook

  Without `--embed-resources`, those CSS and JavaScript use their main cloud CDN URLs, and therefore require Internet connection to view the generated documents.

  The embedded version of the document can be viewed offline however.

  There is however a known bug: KaTeX fonts are not currently embedded, so math won't work properly. The situation is similar as for images, but a bit harder because we also need to fetch the blobs from the CSS, which is likely doable from Webpack:
  - [https://github.com/ourbigbook/ourbigbook/issues/157](https://github.com/ourbigbook/ourbigbook/issues/157)
  - [https://stackoverflow.com/questions/41657087/webpack-inline-font-with-url-loader](https://stackoverflow.com/questions/41657087/webpack-inline-font-with-url-loader)
  - [https://stackoverflow.com/questions/35369419/how-to-use-images-in-css-with-webpack](https://stackoverflow.com/questions/35369419/how-to-use-images-in-css-with-webpack)

Examples of embedding that could be implemented in the future:
- [images](image.md) are downloaded if needed and embedded as `data:` URLs.

  Doing this however has a downside: it would slow the page loading down. The root problem is that HTML was not designed to contain assets, and notably it doesn't have byte position indices that can tell it to skip blobs while parsing, and how to refer to them later on when they show up on the screen. This is kind of why EPUB exists: [https://github.com/ourbigbook/ourbigbook/issues/158](https://github.com/ourbigbook/ourbigbook/issues/158)

  Images that are managed by the project itself and already locally present, such as those inside the project itself or due to [`media-providers`](ourbigbook-json/media-providers.md) usually don't require download.

  For images linked directly from the web, we maintain a local download cache, and skip downloads if the image is already in the cache.

  To re-download due to image updates, use either:
  - `--asset-cache-update`: download all images such that the local disk timestamp is older than the HTTP modification date with [`If-Modified-Since`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Modified-Since)
  - `--asset-cache-update-force`: forcefully redownload all assets

Keep in mind that certain things can never be embedded, e.g.:
- YouTube videos, since YouTube does not offer any download API

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [`--embed-includes`](embed-includes.md)
- [Produce a standalone HTML file](produce-a-standalone-html-file.md)
- [Useless knowledge](useless-knowledge.md)
