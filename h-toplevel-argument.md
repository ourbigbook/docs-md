# `\H` `toplevel` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)  
🏷️ **Tags:** [Boolean argument](boolean-argument.md)

When the `\H` `toplevel` argument is set, the header and its descendants will be automatically output to a separate file, even without [`-S`, `--split-headers`](split-headers.md).

For example given:

animal.bigb
```
= Animal

== Vertebrate

=== Dog
{toplevel}

==== Bulldog

== Invertebrate
```

and if you convert as:
```
ourbigbook animal.bigb
```
we get the following output files:
- `animal.html`: contains the headers: "Animal", "Vertebrate" and "Invertebrate", but not "Dog" and "Bulldog"
- `dog.html`: contains only the headers: "Dog" and "Bulldog"

This option is intended to produce output identical to using [includes](include.md) and separate files, i.e. the above is equivalent to:

animal.bigb
```
= Animal

== Vertebrate

\Include[dog]

== Invertebrate
```

dog.bigb
```
= Dog
{toplevel}

== Bulldog
```

Or in other words: [the toplevel header](the-toplevel-header.md) of each source file gets `{toplevel}` set implicitly for it by default.

This design choice might change some day. Arguably, the most awesome setup is on in which source files and outputs are completely decoupled. [OurBigBook Web](ourbigbook-web.md) also essentially wants this, as ideally we want to store one source per header there in each DB entry. We shall see.

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
