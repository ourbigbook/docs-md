<h1 id="input-format-md"><code>--input-format md</code></h1>

↑ **Parent:** [`-I --input-format <inputformat>`](input-format.md)

OurBigBook has some level of support for markdown input.

Markdown wikilinks use native OurBigBook cross-reference resolution: `[[fundamental theorem of calculus]]` is equivalent to `<fundamental theorem of calculus>`, and `[[my id|my text]]` is equivalent to `<my id>[my text]`. Custom display text can contain Markdown. Wikilinks remain literal inside code; escape the first bracket as `\[[my id]]` to display the syntax in normal text.

You can transparently [include](include.md) standard markdown files such as [markdown-example.md](markdown-example.md) with:
```
\Include[markdown-example]
```
and OurBigBook will integrate it into the current project seamlessly. Live demo:

**Table of contents**

- [Markdown example](markdown-example.md)
  - [OurBigBook Markdown extensions](markdown-example.md#ourbigbook-markdown-extensions)
    - [Markdown example child](markdown-example-child.md)
    - [OurBigBook Markdown shorthand extensions](markdown-example.md#ourbigbook-markdown-shorthand-extensions)
      - [OurBigBook Markdown wikilinks](markdown-example.md#ourbigbook-markdown-wikilinks)
    - [OurBigBook Markdown extensions h3](markdown-example.md#ourbigbook-markdown-extensions-h3)
      - [OurBigBook Markdown extensions h4](markdown-example.md#ourbigbook-markdown-extensions-h4)
        - [OurBigBook Markdown extensions h5](markdown-example.md#ourbigbook-markdown-extensions-h5)
          - [OurBigBook Markdown extensions h6](markdown-example.md#ourbigbook-markdown-extensions-h6)
            - [OurBigBook Markdown extensions h7](markdown-example.md#ourbigbook-markdown-extensions-h7)
              - [OurBigBook Markdown extensions h8](markdown-example.md#ourbigbook-markdown-extensions-h8)

## ↑ Ancestors (4)

1. [`-I --input-format <inputformat>`](input-format.md)
2. [OurBigBook CLI options](ourbigbook-cli-options.md)
3. [OurBigBook CLI](ourbigbook-cli.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`-I --input-format <inputformat>`](input-format.md)
