# `\x` within `title` restrictions

↑ **Parent:** [Internal link](internal-link.md)

If you use an [internal link](internal-link.md) within a [`title` argument](title-argument.md), that can generate complex dependencies between IDs, which would either be harder to implement, or lead to infinite recursion.

To prevent such problems:
- for the case of [headers](header.md):
  - if the [internal link](internal-link.md) text is explicitly given, then it is used to calculate the ID of the title element and on render output
  - otherwise, the href argument is used for the ID and the render output. This generally works best when you use [magic links](x-magic-argument.md).
- for non-[headers](header.md) such as [images](image.md), you you can link to headers, and the rendered target gets used for both ID and rendered content

Here are some example:
- 
  ```
  = Hello \x[h2-id][the content]

  == H2 title
  {id=h2-id}
  ```


  - h1 id: `hello-the-content`
  - h1 render content: `Hello the content`
- ```
  = Hello \x[h2-id]

  == H2 title
  {id=h2-id}
  ```


  - h1 id: `hello-h2-id`
  - h1 render content: `Hello h2-id`. Note that this is not very nice due to the `-`, but it can be made nicer without repetition with a [magic link](x-magic-argument.md) as in the following example
- ```
  = Hello <blue dog>

  == Blue dog
  ```


  - h1 id: `hello-blue-dog`
  - h1 render content: `Hello blue dog`
- non-header (e.g. an [image](image.md)) that links to the title of another non-header

  For non-headers, things are a bit more relaxed, and we can link to headers, e.g.:
  ```
  = h1

  \Image[myimg.jpg]
  {title=my \x[h1]}
  ```
  This is allowed because OurBigBook calculates IDs in two stages: first for all headers, and only later non non-headers.

  What you cannot do is link to another image e.g.:
  ```
  \Image[myimg.jpg]
  {id=myimage1}
  {title=My image 1}

  \Image[myimg.jpg]
  {title=my \x[h1]}
  ```
  and there the workaround are much the same as for headers: either explicitly set the [internal link](internal-link.md) content:
  ```
  \Image[myimg.jpg]
  {id=myimage1}
  {title=My image 1}

  \Image[myimg.jpg]
  {title=my \x[h1][My image 1]}
  ```
  or explicitly set an ID:
  ```
  \Image[myimg.jpg]
  {id=myimage1}
  {title=My image 1}

  \Image[myimg.jpg]
  {id=myimage2}
  {title=my \x[h1]}
  ```
  TODO both workaround are currently broken [Image title with x to image with content incorrectly disallowed](todo/image-title-with-x-to-image-with-content-incorrectly-disallowed.md), we forgot to add a test earlier on, and things inevitably broke... Should not be hard to fix though, we are just overchecking.

While it is technically possible relax the above limitations and give an error only in case of loops, it would require a bit of extra work which we don't want to put in right now: [https://github.com/ourbigbook/ourbigbook/issues/95](https://github.com/ourbigbook/ourbigbook/issues/95).

Furthermore, the above rules do not exclude infinite rendering loops, but OurBigBook detects such loops and gives a nice error message, this has been fixed at: [https://github.com/ourbigbook/ourbigbook/issues/34](https://github.com/ourbigbook/ourbigbook/issues/34)

For example this would contain an infinite loop:
```
\Image[myimg.jpg]
{id=myimage1}
{title=\x[myimage2]}

\Image[myimg.jpg]
{id=myimage2}
{title=\x[myimage1]}
```

This infinite recursion is fundamentally not technically solved: the user has to manually break the loop by providing an `x` content explicitly, e.g. in either:
```
\Image[myimg.jpg]
{id=myimage1}
{title=\x[myimage2][my content 2]}

\Image[myimg.jpg]
{id=myimage2}
{title=\x[myimage1]}
```
or:
```
\Image[myimg.jpg]
{id=myimage1}
{title=\x[myimage2]}

\Image[myimg.jpg]
{id=myimage2}
{title=\x[myimage1][my content 1]}
```

A closely related limitation is the simplistic approach to [`\x` `id` output format](x-id-output-format.md).

## ↑ Ancestors (4)

1. [Internal link](internal-link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Conversion process overview](conversion-process-overview.md)
- [`--format-source`](format-source.md)
- [`\x` `id` output format](x-id-output-format.md)
