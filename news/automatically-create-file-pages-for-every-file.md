<h1 id="automatically-create-file-pages-for-every-file">Automatically create <code>_file</code> pages for every file</h1>

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [Static website](../p-publish.md)

<a id="_399"></a>
Previously we would only create an entry in the [`_file` output directory](../file-output-directory.md) for [headers](../header.md) marked wiht the [`\H` `file` argument](../h-file-argument.md).

<a id="_400"></a>
For example the file [file_demo/hello_world.js](file_demo/hello_world.js) in this repository has an associated header with the `file` argument in our [index.bigb](index.bigb) :<a id="_401"></a>

```
= file_demo/hello_world.js
{file}

An explanation of what this text file is about.

Another line.
```

<a id="_402"></a>
As a result, when doing a [split header](../split-headers.md) conversion, it would get both:<a id="_403"></a>

<a id="_404"></a>
- a [`_file` output directory](../file-output-directory.md) page at path `_file/file_demo/hello_world.js` [file\_demo/hello\_world.js](../_file/file_demo/hello_world.js.md)
<a id="_405"></a>
- a [`_raw` directory](../raw-directory.md) page at path `_raw/file_demo/hello_world.js` [file_demo/hello_world.js](file_demo/hello_world.js)

<a id="_406"></a>
On the other hand, the test file [file_demo/nofile.js](file_demo/nofile.js) has no such associated header in the source code.

<a id="_407"></a>
Before this change, [file_demo/nofile.js](file_demo/nofile.js) would only get an [`_raw` directory](../raw-directory.md) entry under `_raw/file_demo/nofile.js` and not `_file` entry. But now it also gets both.

<a id="_408"></a>
The advantages of a `_file` entries over `_raw` entries are as follows:<a id="_409"></a>

<a id="_410"></a>
- `_file` entries can have metadata such as:<a id="_411"></a>

  <a id="_412"></a>
  - OurBigBook content associated to them when they have an associated `_file` header. For example at [file\_demo/hello\_world.js](../_file/file_demo/hello_world.js.md) we can see the rendered text:<a id="_413"></a>
    > <a id="_414"></a>
    > An explanation of what this text file is about.
    > 
    > <a id="_415"></a>
    > Another line.

    Of course, in that case, they would also get the `_file` entry even before this update. However, this update does allow for a smooth update path where you can first link to the `_file` entry from external websites, and then add comments as needed later on without changing URLs.
  <a id="_416"></a>
  - Google Analytics and other features via [ourbigbook.liquid.html](../ourbigbook-liquid-html.md)
<a id="_417"></a>
- `_file` always shows on static website hosts like GitHub Pages, since they are just HTML pages. This is unlike `raw` files which may just get downloaded for unknown extensions like `.bigb` rather than displayed on the browser: [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](../raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages.md)

<a id="_418"></a>
This change is especially powerful following [Always show large text files on `_file` split headers](always-show-large-text-files-on-file-split-headers.md).

<a id="_419"></a>
Because we now have `_file` entries for every single file, we have also modified [`_dir` directory](../dir-directory.md) directory listing pages to link to `_file` entries as those are generally more useful than `_raw` which is what they previously linked to. And you can always reach `_reaw_` from the corresponding `_file` is needed. Example: [https://docs.ourbigbook.com/_dir](https://docs.ourbigbook.com/_dir)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
