<h1 id="escape-literal"><code>--escape-literal</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Take input from stdin as a plaintext string and produce output escaping the input string so that OurBigBook conversion will result in a single output string. E.g.:
```
printf '\\a[`\n' | ourbigbook --escape-literal
```
outputs:
```
\\a\[\`\
```
so that every [character that needed to be escaped](escape-characters.md) was fully escaped to produce plaintext output.

Note that newlines are also currently escaped even when that is not strictly needed, e.g. in the case of double newlines it would be needed but not for single newlines. But we are keeping it simple for now.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)
