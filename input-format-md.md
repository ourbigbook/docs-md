<h1 id="input-format-md"><code>--input-format md</code></h1>

↑ **Parent:** [`-I --input-format <inputformat>`](input-format.md)

OurBigBook has some level of support for markdown input.

Single newlines preserve paragraph grouping, including around fenced code and native block macros; blank lines separate paragraphs. This allows block content inside paragraphs without explicit `\P` wrappers. Unlike standard Markdown's lazy continuation, unindented prose ends a list, and unquoted prose ends a block quote. Indent every continuation line of a list item and prefix every line of a block quote with `>`. This keeps following prose outside those containers without forcing a paragraph break. OurBigBook macro arguments can themselves contain Markdown. The [`github-md` output format](github-md-output-format.md) is for GitHub deployment, not lossless conversion to editable Markdown source.

Markdown wikilinks use native OurBigBook cross-reference resolution: `[[fundamental theorem of calculus]]` is equivalent to `<fundamental theorem of calculus>`, and `[[my id|my text]]` is equivalent to `<my id>[my text]`. Custom display text can contain Markdown. Wikilinks remain literal inside code; escape the first bracket as `\[[my id]]` to display the syntax in normal text.

Topic links use `[[#personal knowledge bases]]`, equivalent to `\x[personal knowledge bases]{topic}`. Use `[[#personal knowledge bases|my text]]` for a custom label. Unlike ordinary wikilinks, topic links do not require a matching local header.

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
