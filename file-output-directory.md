<h1 id="file-output-directory"><code>_file</code> output directory</h1>

↑ **Parent:** [`\a` `external` argument](a-external-argument.md)

Analogous to the [`_raw` directory](raw-directory.md), but contains an HTML page that displays the contents of the file inside of it.

As such, unlike in the [`_raw` directory](raw-directory.md) which just contains the file raw, the page can also contain useful metadata about the file, such as:
- its location in the file tree pointing to the [`_dir` directory](dir-directory.md)
- [ourbigbook.liquid.html](ourbigbook-liquid-html.md) elements such as a commenting system like [Giscus](https://ourbigbook.com/go/topic/giscus) and analytics like [Google Analytics](https://ourbigbook.com/go/topic/google-analytics)

If the file has a corresponding [`\H` `file` argument](h-file-argument.md) section, and when using [`-S`, `--split-headers`](split-headers.md), then the content of the corresponding section are shown. Otherwise, only the file is shown.

## ↑ Ancestors (6)

1. [`\a` `external` argument](a-external-argument.md)
2. [`\a` argument](a-argument.md)
3. [Link](link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [`\H` `file` argument](h-file-argument.md)
- [Automatically create `_file` pages for every file](news/automatically-create-file-pages-for-every-file.md)
- [Template variable](template-variable.md)
