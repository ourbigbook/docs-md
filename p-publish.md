<h1 id="p-publish"><code>-p</code>, <code>--publish</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)  
🏷️ **Tags:** [Publish your content](publish-your-content.md)

OurBigBook tooling is so amazing that we also take care of the HTML publishing for you!

Once a publish target is properly setup, all you have to do is run:
```
git add index.bigb
git commit -m 'more content!'
ourbigbook --publish
```
and your changes will be published to the  default target specified in [`ourbigbook.json`](ourbigbook-json.md).

If not specified, e.g. with the the [`--publish-target`](publish-target.md) option, the default target is to [publish to GitHub Pages](publish-target-github-pages.md).

Only changes committed to Git are pushed.

Files that `ourbigbook` knows how to process get processed and only their outputs are added to the published repo, those file types are:
- `.bigb` files are converted to `.html`
- `.scss` files are converted to `.css`
Every other Git-tracked file is pushed as is.

When `--publish` is given, stdin input is not accepted, and so the current directory is built by default, i.e. the following two are equivalent:
```
./ourbigbook --publish
./ourbigbook --publish .
```

Publishing only happens if the build has no errors.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
