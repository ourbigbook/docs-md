<h1 id="publish-commit"><code>-P, --publish-commit &lt;commit-message&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Like the [`--publish` option](p-publish.md), but also automatically:
- `git add -u` to automatically add change to any files that have been previously git tracked
- `git commit -m <commit-message>` to create a new commit with those changes

This allows you to publish your changes live in a single command such as:
```
ourbigbook --publish-commit 'my amazing change' .
```

With great power comes great responsibility of course, but who cares!

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Play with the template](play-with-the-template.md)
