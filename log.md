<h1 id="log"><code>--log</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Give multiple times to enable a list of certain types of logs to stderr help debugging, e.g.:
```
./ourbigbook --log ast tokens -- index.bigb
```
Note that this follows [commander.js' shorthand variadic argumentso syntax](https://github.com/tj/commander.js/tree/e0e723810357e915210af38ccf5098ffe1fb8e65#variadic-option), and thus the `--` is required above. If you want to omit it for a single value you have to add the `=` sign as in:
```
./ourbigbook --log=ast index.bigb
```

Values not documented in other sections:
- `ast`: the full final parsed [abstract syntax tree](abstract-syntax-tree.md) as JSON
- `ast-simple`: a simplified view of the [abstract syntax tree](abstract-syntax-tree.md) with one AstNode or AstArgument per line and showing only the most important fields
- `ast-pp-simple`: view snapshots of the various [abstract syntax tree](abstract-syntax-tree.md) post process stages, more info at: [conversion process overview](conversion-process-overview.md)
- `ast-inside`: print the AST from inside the `ourbigbook.convert` call before it returns.

  This is useful to debug the program if `ourbigbook.convert` blows up on the next stages before returning.
- `db`: show database transactions done by OurBigBook, to help debug stuff like [cross file internal links](cross-file-internal-link.md)
- `mem`: show process memory usage as per Node.js' `process.memoryUsage()` after each [`--log perf`](log-perf.md) step: [https://stackoverflow.com/questions/12023359/what-do-the-return-values-of-node-js-process-memoryusage-stand-for](https://stackoverflow.com/questions/12023359/what-do-the-return-values-of-node-js-process-memoryusage-stand-for). Implies [`--log perf`](log-perf.md).

  To use this options, you must run OurBigBook with the `--expose-gc` command line option, e.g. with:
  ```
  node --expose-gc $(which ourbigbook) myfile.bigb
  ```
- `parse`: parsing steps
- `split-headers`: log which split header is currently being rendered. This can be extremelly helpful to identify which logs that we've added that come from the header of interest.
- `tokenize`: tokenization steps
- `tokens`: final parsed token stream
- `tokens-inside`: like `ast-inside` but for tokens.

  Also adds token index to the output, which makes debugging the parser way easier.

**Table of contents**

- [`--log headers`](log-headers.md)
- [`--log perf`](log-perf.md)

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Abstract syntax tree](abstract-syntax-tree.md)
- [Conversion process overview](conversion-process-overview.md)
