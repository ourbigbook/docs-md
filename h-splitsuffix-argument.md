# `\H` `splitSuffix` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

If given, add a custom suffix to the output filename of the header when using [`-S`, `--split-headers`](split-headers.md).

If the given suffix is empty, it defaults to `-split`.

For example, given:
```
= my h1

== my h2
```
a `--split-headers` conversion would normally place `my h2` into a file called:
```
my-h2.html
```
However, if we instead wrote:
```
== my h2
{splitSuffix}
```
it would not be placed under:
```
my-h2-split.html
```
and if we set a custom one as:
```
== my h2
{splitSuffix=asdf}
```
it would go instead to:
```
my-h2-asdf.html
```

This option is useful if the root of your website is written in OurBigBook, and you want to both:
- have a section that talks about some other project
- host the documentation of that project inside the project source tree

For example, [https://cirosantilli.com](https://cirosantilli.com) with source at [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) has a quick section about OurBigBook: [https://cirosantilli.com#ourbigbook](https://cirosantilli.com#ourbigbook).

Therefore, without a custom suffix, the split header version of that header would go to [https://docs.ourbigbook.com](https://docs.ourbigbook.com), which would collide with this documentation, that is present in a separate repository: [https://github.com/ourbigbook/ourbigbook](https://github.com/ourbigbook/ourbigbook).

Therefore a `splitSuffix` property is used, making the split header version fall under `/ourbigbook-split`, and leaving the nicer `/ourbigbook` for the more important project toplevel.

If given on the [the toplevel headers](the-toplevel-header.md), which normally gets a suffix by default to differentiate from the non-split version, it replaces the default `-split` suffix with a custom one.

For example if you had `notindex.bigb` as:
```
= Not index
```
then it would render to:
```
notindex-split.bigb
```
but if you used instead:
```
= Not index
{splitSuffix=asdf}
```
then it would instead be:
```
notindex-asdf.bigb
```

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [`-S`, `--split-headers`](split-headers.md)
