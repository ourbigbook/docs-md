# `\H` `numbered` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

This [boolean argument](boolean-argument.md) determines whether renderings of a header will have section numbers or not. This affects all of:
- [headers](header.md) themselves
- [table of contents](table-of-contents.md) links
- [internal links](internal-link.md) with the [`\x` `full` argument](x-full-argument.md)
This option can be set by default for all files with:

By default, headers are numbered as in a book, e.g.:
```
= h1

== h2

=== h3

==== h4
```
renders something like:
```
= h1

Table of contents
* 1. h2
  * 1.1. h3
    * 1.1.1. h4

== 1. h2

=== 1.1. h3

==== 1.1.1. h4
```

However, for documents with a very large number of sections, or [deeply nested headers](unlimited-header-levels.md) those numbers start to be more noise than anything else, especially in the table of contents and you are better off just referring to IDs. E.g. imagine:
```
1.3.1.4.5.1345.3.2.1. Some deep level
```

When documents reach this type of scope, you can disable numbering with the `numbered` option.

This option can be set on any header, and it is inherited by all descendants.

The option only affects descendants.

E.g., if in the above example turn numbering off at `h2`:
```
= h1

== h2
{numbered=0}

=== h3

==== h4
```
then it renders something like:
```
= h1

Table of contents
* 1. h2
  * h3
    * h4

== 1. h2

=== h3

==== h4
```

The more common usage pattern to disable it on toplevel and enable it only for specific "tutorial-like sections". An example can be seen at:
- [https://cirosantilli.com/](https://cirosantilli.com/): huge toplevel wiki, for which we don't want numbers
- [https://cirosantilli.com/x86-paging](https://cirosantilli.com/x86-paging): a specific tutorial, for which we want numbers
which is something like:
```
= Huge toplevel wiki
{numbered=0}

== h2

=== A specific tutorial
{numbered}
{scope}

==== h4

===== h5
```
then it renders something like:
```
= Huge toplevel wiki

Table of contents
* h2
  * A specific tutorial
    * 1. h4
      * 1.1.  h5

== h2

=== A specific tutorial

==== 1. h4

===== 1.1. h5
```
Note how in this case the number for `h4` is just `1.` rather than `1.1.1.`. We only show numberings relative to the first non-numbered header, because the `1.1.` wouldn't be very meaningful otherwise.

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`Numbered`](ourbigbook-json/h/numbered.md)
- [`SplitDefault`](ourbigbook-json/h/splitdefault.md)
