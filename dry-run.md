<h1 id="dry-run"><code>--dry-run</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

The `--dry-run` option is a good way to debug the [`--publish` option](p-publish.md), as it builds the publish output files without doing any git commands that would be annoying to revert. So after doing:
```
ourbigbook --dry-run --publish .
```
you can just go and inspect the generated HTML to see what would get pushed at:
```
cd _out/publish/_out/publish/
```
see also: [the `_out` directory](the-out-directory.md).

Inspiration: [https://github.com/cirosantilli/linux-kernel-module-cheat/tree/6d0a900f4c3c15e65d850f9d29d63315a6f976bf#dry-run-to-get-commands-for-your-project](https://github.com/cirosantilli/linux-kernel-module-cheat/tree/6d0a900f4c3c15e65d850f9d29d63315a6f976bf#dry-run-to-get-commands-for-your-project)

**Table of contents**

- [`--dry-run-push`](dry-run-push.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--dry-run-push`](dry-run-push.md)
