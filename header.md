# Header

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Block macro](block-macro.md)

[Shorthand syntax](macro-shorthand-syntax.md) with `= ` (equal sign followed by a space):
```
= My h1

== My h2

=== My h3
```
Shorthand headers end at the first newline found. They cannot therefore contain raw newline tokens.

Equivalent sane:
```
\H[1][My h1]

\H[2][My h2]

\H[3][My h3]
```

Custom ID for [internal links](internal-link.md) on shorthand headers:
```
= My h1
{id=h1}

== My h2
{id=h2}

=== My h3
{id=h3}
```

Sane equivalent:
```
\H[1][My h1]{id=h1}

\H[2][My h2]{id=h2}

\H[3][My h3]{id=h3}
```

**Table of contents**

- [Unlimited header levels](unlimited-header-levels.md)
  - [My h3](my-h3.md)
    - [My h4](my-h4.md)
      - [My h5](my-h5.md)
        - [My h6](my-h6.md)
          - [My h7](my-h7.md)
            - [My h8](my-h8.md)
              - [My h9](my-h9.md)
                - [My h10](my-h10.md)
                  - [My h11](my-h11.md)
                    - [My h12](my-h12.md)
                      - [My h13](my-h13.md)
- [Skipping header levels](skipping-header-levels.md)
- [The toplevel header](the-toplevel-header.md)
  - [The toplevel header IDs don't show](the-toplevel-header-ids-don-t-show.md)
  - [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)
- [`\H` arguments](h-arguments.md)
  - [`\H` `c` argument](h-c-argument.md)
  - [`\H` `child` argument](h-child-argument.md)
  - [`\H` `created` argument](h-created-argument.md)
  - [`\H` `file` argument](h-file-argument.md)
    - [`\H` `file` argument toplevel header](h-file-argument-toplevel-header.md)
    - [Interaction between `{file}` and `{scope}`](interaction-between-file-and-scope.md)
    - [`_file` input directory](file-input-directory.md)
    - [`\H` `file` argument demo](h-file-argument-demo.md)
      - [file\_demo](_file/file_demo.md)
      - [file\_demo/file\_demo\_subdir](_file/file_demo/file_demo_subdir.md)
      - [file\_demo/hello\_world.js](_file/file_demo/hello_world.js.md)
      - [file\_demo/file\_demo\_subdir/hello\_world.js](_file/file_demo/file_demo_subdir/hello_world.js.md)
      - [index.js](_file/index.js.md)
      - [file\_demo/my.bin](_file/file_demo/my.bin.md)
      - [Tank\_man\_standing\_in\_front\_of\_some\_tanks.jpg](_file/Tank_man_standing_in_front_of_some_tanks.jpg.md)
      - [Tank Man by CNN (1989)](_file/https:/www.youtube.com/watch?v=YeFzeNAHEhU.md)
      - [https://example.com](_file/https:/example.com.md)
  - [`\H` `numbered` argument](h-numbered-argument.md)
  - [`\H` `parent` argument](h-parent-argument.md)
    - [ID-based header levels and scope resolution](id-based-header-levels-and-scope-resolution.md)
    - [Header explicit levels vs nesting design choice](header-explicit-levels-vs-nesting-design-choice.md)
  - [`\H` `scope` argument](h-scope-argument.md)
    - [`scope` resolution](scope-resolution.md)
    - [Directory-based `scope`](directory-based-scope.md)
    - [Test scope 1](test-scope-1.md)
      - [Test scope 2](test-scope-1/test-scope-2.md)
        - [Not scoped](test-scope-1/test-scope-2/not-scoped.md)
    - [`\H` `scope` argument of toplevel headers](h-scope-argument-of-toplevel-headers.md)
  - [`\H` `splitDefault` argument](h-splitdefault-argument.md)
  - [`\H` `splitSuffix` argument](h-splitsuffix-argument.md)
  - [`\H` `synonym` argument](h-synonym-argument.md)
  - [`\H` `synonymNoScope` argument](h-synonymnoscope-argument.md)
  - [`\H` `title` argument](h-title-argument.md)
    - [Automatic ID from title](automatic-id-from-title.md)
    - [ID target from title](id-target-from-title.md)
  - [`\H` `tag` argument](h-tag-argument.md)
  - [`\H` `title2` argument](h-title2-argument.md)
    - [`\H` `title2` argument of a synonym header](h-title2-argument-of-a-synonym-header.md)
  - [`\H` `toplevel` argument](h-toplevel-argument.md)
  - [`\H` `updated` argument](h-updated-argument.md)
  - [`\H` `wiki` argument](h-wiki-argument.md)
    - [Tiananmen Square](wiki-explicit.md)
    - [Tiananmen Square](wiki-implicit.md)
    - [History of Tiananmen Square](wiki-explicit-subsection.md)
- [Table of contents](table-of-contents.md)
  - [Table of contents JavaScript open close interaction](table-of-contents-javascript-open-close-interaction.md)
- [Header metadata section](header-metadata-section.md)
  - [Incoming links](incoming-links.md)
  - [Tagged metadata section](tagged-metadata-section.md)
  - [Ancestors](ancestors.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (27)

- [OurBigBook Project](split.md)
- [Argument newlines between arguments removal](argument-newlines-between-arguments-removal.md)
- [Block vs inline macros](block-vs-inline-macros.md)
- [Boolean argument](boolean-argument.md)
- [Escape characters](escape-characters.md)
- [Features](features.md)
- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `parent` argument](h-parent-argument.md)
- [`\H` `scope` argument](h-scope-argument.md)
- [`\H` `title2` argument](h-title2-argument.md)
- [Horizontal rule](horizontal-rule.md)
- [Inline user-defined LaTeX macros](inline-user-defined-latex-macros.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [Local header deletion on web upload](local-header-deletion-on-web-upload.md)
- [Mandatory positional arguments](mandatory-positional-arguments.md)
- [Automatically create `_file` pages for every file](news/automatically-create-file-pages-for-every-file.md)
- [`Lint` `h-tag`](ourbigbook-json/lint-h-tag.md)
- [`Redirects`](ourbigbook-json/redirects.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
- [Positional vs named arguments](positional-vs-named-arguments.md)
- [Secondary children](secondary-children.md)
- [Table of contents JavaScript open close interaction](table-of-contents-javascript-open-close-interaction.md)
- [`title` argument](title-argument.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
- [`\x` `file` argument](x-file-argument.md)
- [`\x` `full` argument](x-full-argument.md)
- [`\x` within `title` restrictions](x-within-title-restrictions.md)
