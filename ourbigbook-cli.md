# OurBigBook CLI

↑ **Parent:** [OurBigBook Project](split.md)

OurBigBook CLI is the executable program called `ourbigbook` which comes when you install `npm install ourbigbook`. It is the main command line utility of the [OurBigBook Project](split.md).

Its functionality will also be exposed on GUI [editor support](editor-support.md) such as [Visual Studio Code](visual-studio-code.md) to make things nicer for non-technical users.

The main functionalities of the executable are to:
- convert [OurBigBook Markup](ourbigbook-markup.md) files to HTML files or other formats

  The HTML files can then be either viewd from your filesystem on a browser, or uploaded and hosted very cheaply or for free so that others can see it, e.g. on [GitHub Pages](publish-target-github-pages.md).
- [publish your content](publish-your-content.md), either to [OurBigBook Web](ourbigbook-web.md) or as a [static website](p-publish.md)

Or if you are a programmer: OurBigBook CLI is a Static Wiki generator that can be invoked from the command line with the [`ourbigbook` executable](ourbigbook-cli.md).

OurBigBook CLI is how [https://cirosantilli.com](https://cirosantilli.com) is published.

OurBigBook Web takes as input the exact same format of OurBigBook Markup files used by OurBigBook CLI. TODO support/improve import/export to/from OurBigBook Web, see also: [`-W`, `--web`](web.md).

The OurBigBook CLI calls the [OurBigBook Library](ourbigbook-library.md) to convert each input file.

Convert a `.bigb` file to HTML and output the HTML to a file with the same basename without extension, e.g.:
```
ourbigbook hello.bigb
firefox _out/html/hello.html
```

Files named `index.bigb` are converted to `index.html` so that they will show on the website's base address:
```
ourbigbook index.bigb
firefox _out/html/index.html
```

Convert all `.bigb` files in a directory to HTML files, e.g. `somefile.bigb` to `_out/html/somefile.html`:
```
ourbigbook .
```
The HTML output files are placed right next to each corresponding `.bigb`.

The output file can be selected explicitly with: [`--outfile <outfie>`](outfile.md).

Output to stdout instead of saving it to a file:
```
ourbigbook --stdout index.bigb
```

In order to resolve [cross file internal links](cross-file-internal-link.md), this actually does two passes:
- first an [ID extraction](id-extraction.md) pass, which parses all inputs and dumps their IDs to the ID database
- then a second render pass, which uses the IDs in the ID database

**Table of contents**

- [stdin conversion](stdin-conversion.md)
- [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)
  - [Play with the template](play-with-the-template.md)
  - [Important command line options](important-command-line-options.md)
    - [Produce a standalone HTML file](produce-a-standalone-html-file.md)
  - [Useless knowledge](useless-knowledge.md)
- [Publish your content](publish-your-content.md)
  - [OurBigBook Web vs static website publishing](ourbigbook-web-vs-static-website-publishing.md)
- [Index file](index-file.md)
  - [Project toplevel directory](project-toplevel-directory.md)
    - [The toplevel index file](the-toplevel-index-file.md)
      - [The home article](the-home-article.md)
      - [The current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)
- [OurBigBook CLI options](ourbigbook-cli-options.md)
  - [`--check-db-only`](check-db-only.md)
  - [`--china`](china.md)
  - [`--dry-run`](dry-run.md)
    - [`--dry-run-push`](dry-run-push.md)
  - [`--embed-includes`](embed-includes.md)
  - [`--escape-literal`](escape-literal.md)
  - [`--embed-resources`](embed-resources.md)
  - [-`F`, `--force-render`](force-render.md)
  - [`--format-source`](format-source.md)
  - [`--generate`](generate.md)
  - [`--help-macros`](help-macros.md)
  - [`--log`](log.md)
    - [`--log headers`](log-headers.md)
    - [`--log perf`](log-perf.md)
  - [`--no-check-db`](no-check-db.md)
  - [`--no-db`](no-db.md)
  - [`--no-html-x-extension`](no-html-x-extension.md)
  - [`--no-render`](no-render.md)
  - [`--no-web-render`](no-web-render.md)
  - [`--outdir <outdir>`](outdir.md)
  - [`--outfile <outfie>`](outfile.md)
  - [`-I --input-format <inputformat>`](input-format.md)
  - [`-O --output-format <outformat>`](output-format.md)
    - [`bigb` output format](bigb-output-format.md)
    - [`html` output format](html-output-format.md)
    - [`md` output format](md-output-format.md)
    - [`adoc` output format](adoc-output-format.md)
    - [`id` output format](id-output-format.md)
      - [`\x` `id` output format](x-id-output-format.md)
      - [Unimplemented output formats](unimplemented-output-formats.md)
        - [`latex` output format](latex-output-format.md)
  - [`-p`, `--publish`](p-publish.md)
  - [`-P, --publish-commit <commit-message>`](publish-commit.md)
  - [`--publish-no-convert`](publish-no-convert.md)
  - [`--publish-target`](publish-target.md)
    - [`--publish-target github-pages`](publish-target-github-pages.md)
      - [Publish to GitHub pages root page](publish-to-github-pages-root-page.md)
      - [`.github` directory is ignored on GitHub Pages](github-directory-is-ignored-on-github-pages.md)
      - [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages.md)
    - [`--publish-target github-md`](publish-target-github-md.md)
    - [`--publish-target local`](publish-target-local.md)
  - [`-S`, `--split-headers`](split-headers.md)
    - [Internal link targets in split headers](internal-link-targets-in-split-headers.md)
  - [`--stdout`](stdout.md)
  - [`--template`](template.md)
    - [ourbigbook.liquid.html](ourbigbook-liquid-html.md)
      - [`rel="canonical"`](rel-canonical.md)
    - [Template variable](template-variable.md)
      - [`publishTargetIsWebsite`](publishtargetiswebsite.md)
  - [`--title-to-id`](title-to-id.md)
  - [`--unsafe-ace`](unsafe-ace.md)
  - [`-w`, `--watch`](watch.md)
  - [`-W`, `--web`](web.md)
    - [Local header deletion on web upload](local-header-deletion-on-web-upload.md)
      - [OurBigBook Web unlisted content](ourbigbook-web-unlisted-articles.md)
  - [`--web-ask-password`](web-ask-password.md)
  - [`--web-dry`](web-dry.md)
  - [`--web-id`](web-id.md)
  - [`--web-force-id-extraction`](web-force-id-extraction.md)
  - [`--web-force-render`](web-force-render.md)
  - [`--web-max-renders`](web-max-renders.md)
  - [`--web-nested-set` (option)](web-nested-set-option.md)
  - [`--no-web-nested-set-bulk`](no-web-nested-set-bulk.md)
  - [`--web-password`](web-password.md)
  - [`--web-test`](web-test.md)
  - [`--web-url`](web-url.md)
  - [`--web-user`](web-user.md)
- [`ourbigbook.json`](ourbigbook-json.md)
  - [`dontIgnore`](ourbigbook-json/dontignore.md)
  - [`dontIgnoreConvert`](ourbigbook-json/dontignoreconvert.md)
  - [`generateSitemap`](ourbigbook-json/generatesitemap.md)
  - [`ignore`](ourbigbook-json/ignore.md)
  - [`ignoreRender`](ourbigbook-json/ignorerender.md)
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
- [Make all links of a static website point to another deployment of the website](make-all-links-of-a-static-website-point-to-another-deployment-of-the-website.md)
- [Ignored files](ignored-files.md)
  - [Ignore from `.gitignore`](ignore-from-gitignore.md)
- [Parallel build](parallel-build.md)
- [OurBigBook CLI test matrix](ourbigbook-cli-test-matrix.md)

## 🏷️ Tagged (1)

- [OurBigBook CLI enforces consistent header tree by default](news/ourbigbook-cli-enforces-consistent-header-tree-by-default.md)

## ↑ Ancestors (1)

1. [OurBigBook Project](split.md)

## ← Incoming links (26)

- [OurBigBook Project](split.md)
- [index.js](_file/index.js.md)
- [Arbitrary code execution](arbitrary-code-execution.md)
- [Built-in LaTeX macros](built-in-latex-macros.md)
- [`convert` function](convert-function.md)
- [Demo data local file output](demo-data-local-file-output.md)
- [`Dist` directory](dist-directory.md)
- [Do the release](do-the-release.md)
- [External link](external-link.md)
- [Inline user-defined LaTeX macros](inline-user-defined-latex-macros.md)
- [Local development server](local-development-server.md)
- [OurBigBook CLI enforces consistent header tree by default](news/ourbigbook-cli-enforces-consistent-header-tree-by-default.md)
- [`_obb` directory](obb-directory.md)
- [`Ignore`](ourbigbook-json/ignore.md)
- [`Web`](ourbigbook-json/web.md)
- [`LinkFromStaticHeaderMetaToWeb`](ourbigbook-json/web/linkfromstaticheadermetatoweb.md)
- [OurBigBook Library environemnt variable](ourbigbook-library-environemnt-variable.md)
- [OurBigBook Markup](ourbigbook-markup.md)
- [OurBigBook Web directory structure](ourbigbook-web-directory-structure.md)
- [OurBigBook Web dynamic article tree](ourbigbook-web-dynamic-article-tree.md)
- [OurBigBook Web restrictions compared to CLI](ourbigbook-web-restrictions-compared-to-cli.md)
- [`--publish-target local`](publish-target-local.md)
- [Quick start](quick-start.md)
- [Subdirectory deployment](subdirectory-deployment.md)
- [UnsafeXss](unsafexss.md)
- [`--web-dry`](web-dry.md)
