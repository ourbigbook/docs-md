<h1 id="publish-target-local"><code>--publish-target local</code></h1>

↑ **Parent:** [`--publish-target`](publish-target.md)

Publish as a local directory that can be zipped and sent to someone else, and then correctly viewed by a browser locally by the receiver. You can then zip it from the Linux command line for example with:
```
ourbigbook --publish --publish-target local
cd _out/publish/_out
zip -r local.zip local
```
Maybe we should do the Zip step from the [OurBigBook CLI](ourbigbook-cli.md) as well. There is no Node.js standard library wrapper however apparently: [https://stackoverflow.com/questions/15641243/need-to-zip-an-entire-directory-using-node-js](https://stackoverflow.com/questions/15641243/need-to-zip-an-entire-directory-using-node-js)

## ↑ Ancestors (4)

1. [`--publish-target`](publish-target.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Publish your content](publish-your-content.md)
