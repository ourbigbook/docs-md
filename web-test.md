<h1 id="web-test"><code>--web-test</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Set defaults for `--web-*` options that are useful for testing locally:
```
ourbigbook --web-test
```
is equivalent to:
```
ourbigbook --web --web-url http://localhost:3000 --web-user barack-obama --web-password asdf
```
You can also override those defaults by just specifying them normally, e.g. to do a different user:
```
ourbigbook --web-test --web-user donald-trump
```

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`--web-ask-password`](web-ask-password.md)
