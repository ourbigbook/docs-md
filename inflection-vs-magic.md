# Inflection vs magic

↑ **Parent:** [Internal link](internal-link.md)

The [`\x` `magic` argument](x-magic-argument.md) was introduced later, and basically became a better alternative to [internal link title inflection](internal-link-title-inflection.md) in all but the following cases:
- [`\H` `disambiguate` argument](disambiguate-argument.md): disambiguate prevents the determination of plural inflection, e.g. in:
  ```
  = Python
  {disambiguate=animal}

  I like <python animal>.
  ```
  there is currently no way to make it output `Pythons` in the plural without resorting to either [`\x` `p` argument](x-p-argument.md) or an explicit content, because if you wrote:
  ```
  I like <pythons animal>.
  ```
  it would just lead to Id not found, as we would try the plural vs singular on `animal` only.

  Maybe one day we can implement an even more shorthand system that understands that parenthesis should skipped for the inflection as in:
  ```
  I like <pythons (animal)>.
  ```
  [https://github.com/ourbigbook/ourbigbook/issues/244](https://github.com/ourbigbook/ourbigbook/issues/244)

- plural headers. We only attempt to singularize arguments for now, not pluralize them. So if you had:
  ```
  My <dog> is nice.

  == Dogs
  ```

  you would instead need to write:
  ```
  My <dog>{p=0} is nice.
  ```

  or:
  ```
  My <dog>[dog] is nice.
  ```

## ↑ Ancestors (4)

1. [Internal link](internal-link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Internal link title inflection](internal-link-title-inflection.md)
- [`\x` `magic` argument](x-magic-argument.md)
