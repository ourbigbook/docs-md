# Produce a standalone HTML file

↑ **Parent:** [Important command line options](important-command-line-options.md)

To produce a single standalone output file that contains everything the viewer needs to correctly see the page do:
```
npx ourbigbook --embed-resources --embed-includes index.bigb
```
You can now just give the generated `_out/html/index.html` to any reader and they should be able to view it offline without installing anything. The flags are:
- [`--embed-includes`](embed-includes.md): without this, `\Include[not-index]` shows as a link to the file `_out/html/not-index.html` which comes from `not-index.bigb` With the flag, `not-index.bigb` output gets embedded into the output `_out/html/index.html` directly
- [`--embed-resources`](embed-resources.md): by default, we link to CSS and JavaScript that lives inside `node_modules`. With this flag, that CSS and JavaScript is copied inline into the document instead. One day we will try to handle [images](image.md) that way as well

## ↑ Ancestors (4)

1. [Important command line options](important-command-line-options.md)
2. [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)
