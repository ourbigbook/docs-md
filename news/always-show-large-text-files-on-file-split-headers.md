<h1 id="always-show-large-text-files-on-file-split-headers">Always show large text files on <code>_file</code> split headers</h1>

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [Static website](../p-publish.md)

<a id="_421"></a>
Previously, large files with an [`\H` `file` argument](../h-file-argument.md) associated to them would show a message<a id="_422"></a>

```
index.js was not rendered because it is too large (> 2000 bytes)
```
rather than the file contents both on their split and non-split versions, e.g.:<a id="_423"></a>

<a id="_424"></a>
- [https://docs.ourbigbook.com/#_file/index.js](https://docs.ourbigbook.com/#_file/index.js)
<a id="_425"></a>
- [https://docs.ourbigbook.com/_file/index.js](https://docs.ourbigbook.com/_file/index.js)

<a id="_426"></a>
Now, the split version [https://docs.ourbigbook.com/_file/index.js](https://docs.ourbigbook.com/_file/index.js) alwayws shows the full text file.

<a id="_427"></a>
When not in split mode, limiting preview sizes is important otherwise multi-header pages might become far too big. Ideally we would have found a way to reliably use `iframe` + `loading="lazy"` to refer to the file without actually embedding it into the page as we do for images, but we haven't managed to do that so far.

<a id="_428"></a>
This allows us to now see files that were previously not visible anywhere on the rendered HTML without download due to [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](../raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages.md).

<a id="_429"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/always-show-large-files-on-split-headers.png" alt="" height="700">

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [Automatically create `_file` pages for every file](automatically-create-file-pages-for-every-file.md)
