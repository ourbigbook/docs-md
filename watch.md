<h1 id="watch"><code>-w</code>, <code>--watch</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Don't quit `ourbigbook` immediately.

Instead, watch the selected file or directory for changes, and rebuild individual files when changes are detected.

Watch every `.bigb` file in an entire directory:
```
ourbigbook --watch .
```
When a directory is given as the input path, this automatically first does an [ID extraction](id-extraction.md) pass on all files to support [cross file internal links](cross-file-internal-link.md).

Now you can just edit any OurBigBook file such has `index.bigb`, save the file in your editor, and refresh the webpage and your change should be visible, no need to run a `ourbigbook` command explicitly every time.

Exit by entering Ctrl + C on the terminal.

Watch a single file:
```
ourbigbook --watch index.bigb
```
When a single file is watched, the reference database is not automatically updated. If it is not already up-to-date, you should first update it with:
```
ourbigbook .
```
otherwise you will just get a bunch of undefined ID errors every time the input file is saved.

TODO: integrate Live Preview: [https://asciidoctor.org/docs/editing-asciidoc-with-live-preview/](https://asciidoctor.org/docs/editing-asciidoc-with-live-preview/) to also dispense the browser refresh.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Features](features.md)
- [`Ignore`](ourbigbook-json/ignore.md)
