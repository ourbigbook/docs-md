# Index file

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

An index file is a file with basename `index.bigb`.

Those basenames have the following magic properties:
- the default output file name for an index file in HTML output is either:
  - `index.html` when in the [project toplevel directory](project-toplevel-directory.md). E.g. `index.bigb` renders to `index.html`. Note that GitHub and many other static website hosts then automatically hide the `index.html` part from the URL, so that your `index.bigb` hosted at `http://example.com` will be accessible simply under `http://example.com` and not `http://example.com/index.html`
  - the name of the subdirectory in which it is located when not in the [project toplevel directory](project-toplevel-directory.md). E.g. `mysubdir/index.bigb` outputs to `mysubdir.html`

    Previously, we had placed the output in `mysubdir/index.html`, but this is not as nice as it makes GitHub pages produce URLs with a trailing slash as `mysubdir/`, which is ugly, see also: [https://stackoverflow.com/questions/5948659/when-should-i-use-a-trailing-slash-in-my-url](https://stackoverflow.com/questions/5948659/when-should-i-use-a-trailing-slash-in-my-url)
- the default [toplevel header](the-toplevel-header.md) ID of an index files is derived from the parent directory basename rather than from the source file basename

**Table of contents**

- [Project toplevel directory](project-toplevel-directory.md)
  - [The toplevel index file](the-toplevel-index-file.md)
    - [The home article](the-home-article.md)
    - [The current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)
- [The toplevel index file](the-toplevel-index-file.md)
