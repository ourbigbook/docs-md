# `publishTargetIsWebsite`

↑ **Parent:** [Template variable](template-variable.md)

`true` iff the [`--publish-target`](publish-target.md) is a standard website, i.e. something that will be hosted publicly on a URL. This is currently `true` for the following publish targets:
- `--publish-target github-pages`
and it is `false` for the following targets:
- `--publish-target github-md`
- `--publish-target local`

This template variable is useful to remove JavaScript elements that only work on public websites and not on `localhost` or `file:`, e.g.:
- Google Analytics
- Giscus

## ↑ Ancestors (5)

1. [Template variable](template-variable.md)
2. [`--template`](template.md)
3. [OurBigBook CLI options](ourbigbook-cli-options.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)
