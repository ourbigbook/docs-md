# Table

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [Macro with shorthand syntax](macro-with-shorthand-syntax.md)

The [shorthand syntax](macro-shorthand-syntax.md) marks:
- headers with `|| ` (pipe, pipe space) at the start of a line
- regular cells with `| ` (pipe, space) at the start of a line
- separates rows with double newline
For example:
```
|| Header 1
|| Header 2

| 1 1
| 1 2

| 2 1
| 2 2
```
which renders as:



> | Header 1 | Header 2 |
> | --- | --- |
> | 1 1 | 1 2 |
> | 2 1 | 2 2 |

Empty cells are allowed without the trailing space however:
```
| 1 1
|
| 1 3

| 2 1
|
| 2 3
```
which renders as:



> | 1 1 |  | 1 3 |
> | --- | --- | --- |
> | 2 1 |  | 2 3 |

Equivalent fully explicit version:
```
\Table[
\Tr[
  \Th[Header 1]
  \Th[Header 2]
]
\Tr[
  \Td[1 1]
  \Td[1 2]
]
\Tr[
  \Td[2 1]
  \Td[2 2]
]
]
```
which renders as:



> | Header 1 | Header 2 |
> | --- | --- |
> | 1 1 | 1 2 |
> | 2 1 | 2 2 |

Any white space indentation inside an explicit `\Tr` can make the code more readable, and is automatically removed from final output due to [`remove_whitespace_children`](remove-whitespace-children.md) which is set for `\Table`.

To pass further arguments to an implicit table such as `title` or `id`, you need to use an explicit `table` macro as in: [Table 3. "My table title"](#table-my-table).
```
\Table
{title=My table title}
{id=table-my-table}
[
|| Header 1
|| Header 2

| 1 1
| 1 2

| 2 1
| 2 2
]
```
which renders as:



> <a id="table-my-table"></a>
> | Header 1 | Header 2 |
> | --- | --- |
> | 1 1 | 1 2 |
> | 2 1 | 2 2 |

We would like to remove that explicit toplevel requirement as per: [https://github.com/ourbigbook/ourbigbook/issues/186](https://github.com/ourbigbook/ourbigbook/issues/186) The rules of when the caption shows up or not similar to those of [images](image.md) as mentioned at [Section "Image caption"](image-caption.md).

Multiple source lines, including paragraphs, can be added to a single cell with shorthand syntax by indenting the cell with exactly two spaces just as for [lists](list.md), e.g.:
```
|| h1
|| h2
|| h3

  h3 2

| 11
| 12

  12 2
| 13

| 21
| 22
| 23
```
which renders as:



> | h1 | h2 | h3 h3 2 |
> | --- | --- | --- |
> | 11 | 12 12 2 | 13 |
> | 21 | 22 | 23 |

Arbitrarily complex nested constructs may be used, e.g. a table inside a list inside table:
```
| 00
| 01

  * l1
  * l2

    | 20
    | 21

    | 30
    | 31

| 10
| 11
```
which renders as:



> | 00 | 01 - l1 - l2   | 20 | 21 |   | --- | --- |   | 30 | 31 | |
> | --- | --- |
> | 10 | 11 |

And now a table outside of [`\OurBigBookExample`](ourbigbookexample.md) to test how it looks directly under [the `\Toplevel` implicit macro](toplevel.md):

<a id="table-my-table-title"></a>
| Header 1 | Header 2 |
| --- | --- |
| 1 1 | 1 2 |
| 2 1 | 2 2 |

And a fully shorthand one:

| Header 1 | Header 2 |
| --- | --- |
| 1 1 | 1 2 |
| 2 1 | 2 2 |

And now a larger one to see how the style is looking:

| Header 1 | Header 2 | Header 3 | Header 4 |
| --- | --- | --- | --- |
| 1 1 | 1 2 | 1 3 | 1 4 |
| 2 1 | 2 2 | 2 3 | 2 4 |
| 3 1 | 3 2 | 3 3 | 3 4 |
| 4 1 | 4 2 | 4 3 | 4 4 |
| 5 1 | 5 2 | 5 3 | 5 4 |
| 6 1 | 6 2 | 6 3 | 6 4 |
| 7 1 | 7 2 | 7 3 | 7 4 |
| 8 1 | 8 2 | 8 3 | 8 4 |

**Table of contents**

- [Table sorting](table-sorting.md)
- [`\Table` argument](table-argument.md)
  - [`\Table` `description` argument](table-description-argument.md)
  - [`\Table` `title` argument](table-title-argument.md)

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [`Auto_parent` macro property](auto-parent.md)
- [Escape characters](escape-characters.md)
- [Macro with shorthand syntax](macro-with-shorthand-syntax.md)
- [OurBigBook Markup quick start](ourbigbook-markup-quick-start.md)
