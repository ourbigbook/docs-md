# Topic link pluralization

↑ **Parent:** [`\x` `topic` argument](x-topic-argument.md)

Unlike local links, it is not possible to automatically determine the exact pluralization of a [topic link](x-topic-argument.md) because:
- it would require communicating with the [OurBigBook Web](ourbigbook-web.md) API, which we could in principle do, but we would rather not have static builds depend on Web instances
- topics can be written by multiple authors, and there could be both plural and singular versions of each topic ID, which makes it hard to determine which one is "correct"

Therefore, it is up to authors to specifically specify the desired pluralization of their topic links:
- by default, topic IDs are automatically singularized, e.g.:
  ```
  <#Many Dogs>
  ```

  renders something like:
  ```
  \a[https://ourbigbook.com/go/topic/many-dog][Many Dogs]
  ```
- to prevent this automatic singularization, use [`\x` `p` argument](x-p-argument.md) with `{p}`, e.g.:
  ```
  <#Many Dogs>{p}
  ```

  renders something like:
  ```
  \a[https://ourbigbook.com/go/topic/many-dogs][Many Dogs]
  ```

  This is unfortunately always necessary for uncountable nouns such as "mathematics":
  ```
  I like #mathematics{p}
  ```

  which renders as:

  > I like [mathematics](https://ourbigbook.com/go/topic/mathematics)

  since our underlying pluralization library [blakeembrey/pluralize](blakeembrey-pluralize.md) cannot handle uncountable nouns reliably.

## ↑ Ancestors (6)

1. [`\x` `topic` argument](x-topic-argument.md)
2. [`\x` arguments](x-arguments.md)
3. [Internal link](internal-link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)
