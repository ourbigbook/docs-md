# Link

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Inline macro](inline-macro.md), [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

[Shorthand](macro-shorthand-syntax.md) autolink, i.e. the link text is the same as the link address:
```
The website http://example.com is cool. See also:

\Q[http://example.com/2]
```
which renders as:



> The website [http://example.com](http://example.com) is cool. See also:
> 
> > [http://example.com/2](http://example.com/2)

Exact parsing rules described at: [Section "Shorthand link parsing rules"](shorthand-link-parsing-rules.md).

Note that the prefixes `http://` and `https://` are automatically removed from the displayed link, since they are so common that they woudly simply add noise.

Equivalent sane version:
```
The website \a[http://example.com] is cool.

\Q[\a[http://example.com/2]]
```
which renders as:



> The website [http://example.com](http://example.com) is cool.
> 
> > [http://example.com/2](http://example.com/2)

Shorthand link with custom text:
```
The website http://example.com[example.com] is cool.
```
which renders as:



> The website [example.com](http://example.com) is cool.

Equivalent sane version:
```
The website \a[http://example.com][example.com] is cool.
```
which renders as:



> The website [example.com](http://example.com) is cool.

If the custom text is empty, an autolink is generated. This is often useful if you want your link to be followed by punctuation:
```
The website is really cool: http://example.com[].
```
which renders as:



> The website is really cool: [http://example.com](http://example.com).

This could also be achieved with the sane syntax of course, but this pattern saves a tiny bit of typing.

Link to a file in the current repository:
```
The file \a[index.js] is cool.
```
which renders as:



> The file [index.js](index.js) is cool.

This links to a raw view of that file.

Link to a directory in the current repository:
```
The directory \a[file_demo] is cooler.
```
which renders as:



> The directory [file_demo](file_demo) is cooler.

This links to an output file that contains a generated directory listing of that directory.

**Table of contents**

- [`\a` argument](a-argument.md)
  - [`\a` `href` argument](a-href-argument.md)
  - [`\a` `ref` argument](a-ref-argument.md)
  - [`\a` `external` argument](a-external-argument.md)
    - [Link to the domain root path](link-to-the-domain-root-path.md)
    - [Subdirectory deployment](subdirectory-deployment.md)
    - [External link](external-link.md)
      - [Internal path links are smart](internal-path-links-are-smart.md)
    - [`_dir` directory](dir-directory.md)
    - [`_file` output directory](file-output-directory.md)
    - [`_raw` directory](raw-directory.md)
    - [URL with protocol](url-with-protocol.md)
- [Shorthand link parsing rules](shorthand-link-parsing-rules.md)
  - [Shorthand link termination character](shorthand-link-termination-character.md)
- [Link percent encoding](link-percent-encoding.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [Block vs inline macros](block-vs-inline-macros.md)
- [Internal link title link removal](internal-link-title-link-removal.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [Positional argument default values](positional-argument-default-values.md)
- [History of Tiananmen Square](wiki-explicit-subsection.md)
