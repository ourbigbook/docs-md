<h1 id="ourbigbook-json"><code>ourbigbook.json</code></h1>

↑ **Parent:** [OurBigBook CLI](ourbigbook-cli.md)

OurBigBook configuration file that affects the behaviour of ourbigbook for all files in the directory.

`ourbigbook.json` not used for input from [stdin](stdin-conversion.md), since we are mostly doing quick tests in that case.

While `ourbigbook.json` is optional, it is used to determine the toplevel directory of a OurBigBook project, which has some effects such as those mentioned at [the toplevel index file](the-toplevel-index-file.md).

Therefore, it is recommended that you always have a `ourbigbook.json` in your project's toplevel directory, even if it is going to be an empty JSON containing just:
```
{}
```

For example, if you convert a file in a subdirectory such as:
```
ourbigbook subdir/notindex.bigb
```
then `ourbigbook` walks up the filesystem tree looking for `ourbigbook.json`, e.g.:
- is there a `./subdir/ourbigbook.json`?
- otherwise, is there a `./ourbigbook.json`?
- otherwise, is there a `../ourbigbook.json`?
- otherwise, is there a `../../ourbigbook.json`?
and so on.

If we reach the root path `/` and no `ourbigbook.json` is found, then we understand that there is no `ourbigbook.json` file present.

**Table of contents**

- [`dontIgnore`](ourbigbook-json/dontignore.md)
- [`dontIgnoreConvert`](ourbigbook-json/dontignoreconvert.md)
- [`generateSitemap`](ourbigbook-json/generatesitemap.md)
- [`ignore`](ourbigbook-json/ignore.md)
- [`ignoreConvert`](ourbigbook-json/ignoreconvert.md)
- [`ourbigbook.json` `id`](ourbigbook-json/id.md)
  - [`id` `normalize` `latin`](ourbigbook-json/id-normalize-latin.md)
    - [Latin normalization](ourbigbook-json/latin-normalization.md)
  - [`id` `normalize` `punctuation`](ourbigbook-json/id-normalize-punctuation.md)
    - [Punctuation normalization](ourbigbook-json/punctuation-normalization.md)
- [`lint`](ourbigbook-json/lint.md)
  - [`lint` `h-parent`](ourbigbook-json/lint-h-parent.md)
  - [`lint` `h-tag`](ourbigbook-json/lint-h-tag.md)
- [`h`](ourbigbook-json/h.md)
  - [`numbered`](ourbigbook-json/h/numbered.md)
  - [`splitDefault`](ourbigbook-json/h/splitdefault.md)
  - [`splitDefaultNotToplevel`](ourbigbook-json/h/splitdefaultnottoplevel.md)
- [`htmlXExtension`](ourbigbook-json/htmlxextension.md)
- [`media-providers`](ourbigbook-json/media-providers.md)
- [`openLinksOnNewTabs`](ourbigbook-json/openlinksonnewtabs.md)
- [`outputOutOfTree`](ourbigbook-json/outputoutoftree.md)
- [`prepublish`](ourbigbook-json/prepublish.md)
- [`publishCommitDate`](ourbigbook-json/publishcommitdate.md)
- [`publishOptions`](ourbigbook-json/publishoptions.md)
- [`target`](ourbigbook-json/target.md)
- [`publishBranch`](ourbigbook-json/publishbranch.md)
- [`publishRemoteUrl`](ourbigbook-json/publishremoteurl.md)
- [`publishRootUrl`](ourbigbook-json/publishrooturl.md)
- [`redirects`](ourbigbook-json/redirects.md)
- [`template`](ourbigbook-json/template.md)
- [`toSplitHeaders`](ourbigbook-json/tosplitheaders.md)
- [`web`](ourbigbook-json/web.md)
  - [`host`](ourbigbook-json/web/host.md)
  - [`hostCapitalized`](ourbigbook-json/web/hostcapitalized.md)
  - [`linkFromStaticHeaderMetaToWeb`](ourbigbook-json/web/linkfromstaticheadermetatoweb.md)
  - [`username`](ourbigbook-json/web/username.md)
- [`xPrefix`](ourbigbook-json/xprefix.md)

## ↑ Ancestors (2)

1. [OurBigBook CLI](ourbigbook-cli.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (12)

- [Cross file internal link internals](cross-file-internal-link-internals.md)
- [Disabled macro argument](disabled-macro-argument.md)
- [Features](features.md)
- [Image lazy loading](image-lazy-loading.md)
- [`Redirects`](ourbigbook-json/redirects.md)
- [`-p`, `--publish`](p-publish.md)
- [Project toplevel directory](project-toplevel-directory.md)
- [`-S`, `--split-headers`](split-headers.md)
- [Stdin conversion](stdin-conversion.md)
- [Template variable](template-variable.md)
- [UnsafeXss](unsafexss.md)
- [Video](video.md)
