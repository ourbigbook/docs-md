<h1 id="outfile"><code>--outfile &lt;outfie&gt;</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Save the output to a given file instead of outputting to stdout:
```
./ourbigbook --outfile not-index.html not-index.bigb
```

The generated output is slightly different than that of:
```
./ourbigbook not-index.bigb > not-index.html
```
because with `--outfile` we know where the output is going, and so we can generate relative includes to default CSS/JavaScript files.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [OurBigBook CLI](ourbigbook-cli.md)
