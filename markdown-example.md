# Markdown example

↑ **Parent:** [`--input-format md`](README.md#input-format-md)

Hello, `markdown`!

Hello multi-line code:

```
def myfunc(i):
    return i + 1
```

And an image:

![](-/raw/logo.png)

**Table of contents**

- [OurBigBook Markdown extensions](#ourbigbook-markdown-extensions)
  - [Markdown example child](markdown-example-child.md)
  - [OurBigBook Markdown shorthand extensions](#ourbigbook-markdown-shorthand-extensions)
    - [OurBigBook Markdown wikilinks](#ourbigbook-markdown-wikilinks)
  - [OurBigBook Markdown extensions h3](#ourbigbook-markdown-extensions-h3)
    - [OurBigBook Markdown extensions h4](#ourbigbook-markdown-extensions-h4)
      - [OurBigBook Markdown extensions h5](#ourbigbook-markdown-extensions-h5)
        - [OurBigBook Markdown extensions h6](#ourbigbook-markdown-extensions-h6)
          - [OurBigBook Markdown extensions h7](#ourbigbook-markdown-extensions-h7)
            - [OurBigBook Markdown extensions h8](#ourbigbook-markdown-extensions-h8)

## OurBigBook Markdown extensions

↑ **Parent:** [Markdown example](markdown-example.md)

You can use any sane named argument that you want:


```
Hello my \b[bold text]!

And here a sane quote:

\Q[Hello world!]
{description=My nice quote. This is also markdown: [link to example](http://example.com) site.}
```
which renders as:



> Hello my **bold text**!
> 
> And here a sane quote:
> 
> > Hello world!

And you can add OurBigBook arguments to shortcut Markup syntax:


```
![](logo.png)
{description=OurBigBook logo with a description!}
```
which renders as:



> ![](-/raw/logo.png)
> 
> **[Figure 1](#-/19)** OurBigBook logo with a description!

### Markdown example child

↑ **Parent:** [OurBigBook Markdown extensions](#ourbigbook-markdown-extensions)

[This section is present in another page, follow this link to view it.](markdown-example-child.md)

### OurBigBook Markdown shorthand extensions

↑ **Parent:** [OurBigBook Markdown extensions](#ourbigbook-markdown-extensions)

#### OurBigBook Markdown wikilinks

↑ **Parent:** [OurBigBook Markdown shorthand extensions](#ourbigbook-markdown-shorthand-extensions)

Analogous to Obsidian, generates [internal cross references](README.md#internal-link):


```
Hello my [[OurBigBook]]!

I like [[headers]].

And here with custom text [[header|fancy headers]].
```
which renders as:



> Hello my [OurBigBook](README.md)!
> 
> I like [headers](README.md#header).
> 
> And here with custom text [fancy headers](README.md#header).

### OurBigBook Markdown extensions h3

↑ **Parent:** [OurBigBook Markdown extensions](#ourbigbook-markdown-extensions)

#### OurBigBook Markdown extensions h4

↑ **Parent:** [OurBigBook Markdown extensions h3](#ourbigbook-markdown-extensions-h3)

##### OurBigBook Markdown extensions h5

↑ **Parent:** [OurBigBook Markdown extensions h4](#ourbigbook-markdown-extensions-h4)

###### OurBigBook Markdown extensions h6

↑ **Parent:** [OurBigBook Markdown extensions h5](#ourbigbook-markdown-extensions-h5)

###### OurBigBook Markdown extensions h7

↑ **Parent:** [OurBigBook Markdown extensions h6](#ourbigbook-markdown-extensions-h6)

###### OurBigBook Markdown extensions h8

↑ **Parent:** [OurBigBook Markdown extensions h7](#ourbigbook-markdown-extensions-h7)

## ↑ Ancestors (5)

1. [`--input-format md`](README.md#input-format-md)
2. [`-I --input-format <inputformat>`](README.md#input-format)
3. [OurBigBook CLI options](README.md#ourbigbook-cli-options)
4. [OurBigBook CLI](README.md#ourbigbook-cli)
5. [OurBigBook Project](README.md)
