# JavaScript redirect to split on missing ID

↑ **Parent:** [Runtime feature](runtime-feature.md)

When you have a document like:

animal.bigb

```
= Animal

== Dog

=== Poodle
```

the version without [`-S`, `--split-headers`](split-headers.md) will contains a valid ID within it:

```
animal.html#poodle
```

However, if at some point you decide that the section `dog` has become too large and want to split it as:

```
= Animal

\Include[dog]
```

and:

dog.bigb

```
= Dog

== Poodle
```

When you do this, it would break liks that users might have shared to `animal.html#poodle`, which is not located at `dog.html#poodle`.

To make that less worse, if [`-S`, `--split-headers`](split-headers.md) are enabled, we check at runtime if the ID `poodle` is present in the output, and if it is not, we redirect to the split page `#poodle` to `poodle.html`.

It would be even more awesome if we were able to redirect to the non-split version as well, `dog.html#poodle`, but that would be harder to implement, so not doing it for now.

## ↑ Ancestors (2)

1. [Runtime feature](runtime-feature.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Link to IDs, not URL path](link-to-ids-not-url-path.md)
