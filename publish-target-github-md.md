<h1 id="publish-target-github-md"><code>--publish-target github-md</code></h1>

↑ **Parent:** [`--publish-target`](publish-target.md)

This output target publishes Markdown to be viewed directly in a GitHub repository.

Sample usage:
```
ourbigbook --publish --publish-target github-md
```

Some demos:
- [https://github.com/ourbigbook/docs-md](https://github.com/ourbigbook/docs-md): a render of this documentation
- [https://github.com/cirosantilli/cirosantilli.github.io-md](https://github.com/cirosantilli/cirosantilli.github.io-md): a render of [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io)

The generated Markdown should be seen primarily as an output format which attempts to render as closely as possible to the corresponding HTML, not as a directly editable canonical input format, as it contains several constructs which are present only to render nicely.

Both nonsplit `.md` documents and the `.md` files produced by [`-S`, `--split-headers`](split-headers.md) are included, cross-file links target those Markdown files, and generated `index.md` files are named `README.md` so directory landing pages work naturally on GitHub.

GitHub documents a general formatted-text preview threshold of approximately 2 MB: [https://docs.github.com/repositories/creating-and-managing-repositories/repository-limits#text-limits](https://docs.github.com/repositories/creating-and-managing-repositories/repository-limits#text-limits) However, repository landing pages truncate README files at 512 KiB: [https://github.com/orgs/community/discussions/23920](https://github.com/orgs/community/discussions/23920) Because this target produces README files, it conservatively applies the lower 512 KiB limit to every generated Markdown file. Where a safe header boundary exists, an oversized nonsplit page is automatically replaced by its split-header version. Its table of contents links included source files to their canonical nonsplit `.md` pages rather than their `-split.md` alternates. If the recursive table of contents would still make a split page too large, only its first child level is included. A single header section that remains too large cannot be split safely, so publication continues with a warning asking for another child header. For testing or a more conservative threshold, `githubMarkdownMaxBytes` may be set under the `github-md` target. Values above the GitHub limit are capped at the built-in limit.

The OurBigBook documentation configures this target to publish to [https://github.com/ourbigbook/docs-md](https://github.com/ourbigbook/docs-md) using [`target`](ourbigbook-json/target.md).

## ↑ Ancestors (4)

1. [`--publish-target`](publish-target.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)
