# Boolean argument

↑ **Parent:** [Macro argument type](macro-argument-type.md)

Name arguments marked in [`--help-macros`](help-macros.md) as `boolean: true` must either:
- take no value and no `=` sign, in which case the value is implicitly set to `1`
- take value exactly `0` or `1`
- not be given, in which case a custom per-macro default is used. That value is the `default` from [`--help-macros`](help-macros.md), or `0` if such default is not given

For example, the [`\x` `full` argument](x-full-argument.md) of [internal links](internal-link.md) is correctly written as:
```
\x[boolean-argument]{full}
```
which renders as:



> [Section "Boolean argument"](boolean-argument.md)

without the `=` sign, or equivalently:
```
\x[boolean-argument]{full=1}
```
which renders as:



> [Section "Boolean argument"](boolean-argument.md)

The `full=0` version is useful in the case of reference targets that unlike [headers](header.md) expand the title on the [internal link](internal-link.md) by default, e.g. [images](image.md):
```
\x[boolean-argument]{full=1}
```
which renders as:



> [Section "Boolean argument"](boolean-argument.md)

The name "boolean argument" is given by analogy to the ["boolean attribute" concept in HTML5](https://stackoverflow.com/questions/16109358/what-is-the-correct-readonly-attribute-syntax-for-input-text-elements/24588427#24588427).

## 🏷️ Tagged (10)

- [`\a` `external` argument](a-external-argument.md)
- [`\a` `ref` argument](a-ref-argument.md)
- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [`\H` `toplevel` argument](h-toplevel-argument.md)
- [Image `border` argument](image-border-argument.md)
- [Image `external` argument](image-external-argument.md)
- [`\x` `magic` argument](x-magic-argument.md)
- [`\x` `p` argument](x-p-argument.md)
- [`\x` `topic` argument](x-topic-argument.md)

## ↑ Ancestors (5)

1. [Macro argument type](macro-argument-type.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (9)

- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `scope` argument](h-scope-argument.md)
- [`\H` `splitDefault` argument](h-splitdefault-argument.md)
- [Image ID](image-id.md)
- [Internal link title inflection](internal-link-title-inflection.md)
- [Positional argument default values](positional-argument-default-values.md)
- [Store images in Wikimedia Commons](store-images-in-wikimedia-commons.md)
- [`\x` `child` argument](x-child-argument.md)
- [`\x` `full` argument](x-full-argument.md)
