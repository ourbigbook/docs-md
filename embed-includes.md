<h1 id="embed-includes"><code>--embed-includes</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Makes [includes](include.md) render the included content in the same output file as the include is located, instead of the default behaviour of creating links.

For example given:

index.bigb
```
= Index

\Include[notindex]
```

notindex.bigb
```
= Notindex

A paragraph in notindex.

== Notindex 2
```

then for conversion with:
```
ourbigbook --embed-includes index.bigb
```
then the output `index.html` contains an output equivalent to if your input file were:
```
= Index

== Notindex

A paragraph in notindex.

=== Notindex 2
```

Note that a prior [ID extraction](id-extraction.md) pass is not required, `--embed-includes` just makes `\Include` read files as they are found in the source.

In addition to this:
- [cross file internal links](cross-file-internal-link.md) outside the included files are disabled, and the cross file ID database does not get updated.

  It should be possible to work around this, but we are starting with the simplest implementation that forbids it. TODO at: [https://github.com/ourbigbook/ourbigbook/issues/343](https://github.com/ourbigbook/ourbigbook/issues/343)

  The problem those cause is that the IDs of included headers show as duplicate IDs of those in the ID database.

  This should be OK to start with because the more common use case with `--html-single-page` is that of including all headers in a single document. TODO: this option is gone.

Otherwise, `include` only adds the headers of the other file to the table of contents of the current one, but not the body of the other file. The ToC entries then point to the headers of the included external files.

You may want to use this option together with [`--embed-resources`](embed-resources.md) to produce fully self-contained individual HTML files for your project.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Conversion process overview](conversion-process-overview.md)
- [Cross file internal link](cross-file-internal-link.md)
- [Features](features.md)
- [Include](include.md)
- [Produce a standalone HTML file](produce-a-standalone-html-file.md)
