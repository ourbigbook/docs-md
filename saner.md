# Saner

↑ **Parent:** [Design goals](design-goals.md)

Originally, OurBigBook was is meant to be both saner and more powerful than Markdown and Asciidoctor.

But alas, as Ciro started implementing and using it, he started to bring some Markdown [syntax sugar he missed back in](macro-shorthand-syntax.md).

And so this "degraded" slightly into a language slightly saner than Asciidoctor but with an amazing Node.js implementation that makes it better for book writing and website publishing.

Notably, we hope that our escaping will be a bit saner backslash escapes everything instead of Asciidoctor's "different escapes for every case" approach: [https://github.com/asciidoctor/asciidoctor/issues/901](https://github.com/asciidoctor/asciidoctor/issues/901)

But hopefully, having starting from a saner point will still produce a saner end result, e.g. there are explicit constructs for every shorthand one.

It is intended that this will be an acceptable downside as OurBigBook will be used primarily large complex content such as books rather than forum posts, and will therefore primarily written either:
- in text editors locally, where users have more features than in random browser textareas
- in a dedicated website that will revolutionize education, and therefore have a good JavaScript editing interface: [https://github.com/cirosantilli/write-free-science-books-to-get-famous-website](https://github.com/cirosantilli/write-free-science-books-to-get-famous-website)

For example, originally OurBigBook had exactly five magic characters, with similar functions as in LaTeX:
- `\` backslash to start a macro, like LaTeX
- `{` and `}`: left and right square brackets to delimit [optional macro arguments](positional-vs-named-arguments.md)
- `[` and `]`: left and right curly braces bracket to start an optional arguments
and double blank newlines for [paragraphs](paragraph.md) if you are pedantic, but this later degenerated into many more with [macro shorthand syntaxes](macro-shorthand-syntax.md).

We would like to have only square brackets for both optional and mandatory to have even less magic characters, but that would make the language difficult to parse for computer and humans. LaTeX was right for once!

This produces a very regular syntax that is easy to learn, including doing:
- arbitrary nesting of elements
- adding arbitrary properties to elements

This sanity also makes the end tail learning curve of the endless edge cases found in Markdown and Asciidoctor disappear.

The language is designed to be philosophically isomorphic to HTML to:
- further reduce the learning curve
- ensure that most of HTML constructs can be reached, including arbitrary nesting

More precisely:
- macro names map to tag names, e.g.: `\\a` to `<a`
- one of the arguments of macros, maps to the content of the HTML element, and the others map to attributes.

  E.g., in a link:
  ```
  \a[http://example.com][Link text\]
  ```
  the first macro argument:
  ```
  http://example.com
  ```
  maps to the `href` of `<a`, and the second macro argument:
  ```
  Link text
  ```
  maps to the internal content of `<a>Link text<>`.

## ↑ Ancestors (3)

1. [Design goals](design-goals.md)
2. [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Design goals](design-goals.md)
- [More powerful](more-powerful.md)
