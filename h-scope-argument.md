# `\H` `scope` argument

↑ **Parent:** [`\H` arguments](h-arguments.md)

In some use cases, the sections under a section describe inseparable parts of something.

For example, when documenting an experiment you executed, you will generally want an "Introduction", then a "Materials" section, and then a "Results" section for every experiment.

On their own, those sections don't make much sense: they are always referred to in the context of the given experiment.

The problem is then how to get unique IDs for those sections.

One solution, would be to manually add the experiment ID as prefix to every subsection, as in:
```
= Experiments

See: \x[full-and-unique-experiment-name/materials]

== Introduction

== Full and unique experiment name

=== Introduction
{id=full-and-unique-experiment-name/introduction}

See our awesome results: \x[full-and-unique-experiment-name/results]

For a more general introduction to all experiments, see: \x[introduction].

=== Materials
{id=full-and-unique-experiment-name/materials}

=== Results
{id=full-and-unique-experiment-name/results}
```

but this would be very tedious.

To keep those IDs shorter, OurBigBook provides the `scope` [boolean argument](boolean-argument.md) property of [headers](header.md), which works analogously to C++ namespaces with the header IDs.

Using `scope`, the previous example could be written more succinctly as:
```
= Experiments

See: \x[full-and-unique-experiment-name/materials]

== Introduction

== Full and unique experiment name
{scope}

=== Introduction

See our awesome results: \x[results]

For a more general introduction to all experiments, see: \x[/introduction].

=== Materials

=== Results
```

Note how:
- full IDs are automatically prefixed by the parent scopes prefixed and joined with a slash `/`
- we can refer to other IDs withing the current scope without duplicating the scope. E.g. `\x[results]` in the example already refers to the ID `full-and-unique-experiment-name/materials`
- to refer to an ID outside of the scope and avoid name conflicts with IDs inside of the current scope, we start a reference with a slash `/`

  So in the example above, `\x[/introduction]` refers to the ID `introduction`, and not `full-and-unique-experiment-name/introduction`.

**Table of contents**

- [`scope` resolution](scope-resolution.md)
- [Directory-based `scope`](directory-based-scope.md)
- [Test scope 1](test-scope-1.md)
  - [Test scope 2](test-scope-1/test-scope-2.md)
    - [Not scoped](test-scope-1/test-scope-2/not-scoped.md)
- [`\H` `scope` argument of toplevel headers](h-scope-argument-of-toplevel-headers.md)

## ↑ Ancestors (5)

1. [`\H` arguments](h-arguments.md)
2. [Header](header.md)
3. [Macro](macro.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
