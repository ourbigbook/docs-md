# `inlineOnly`

↑ **Parent:** [Macro argument property](macro-argument-property.md)

A macro argument property that is `inlineOnly` can only contain [inline macros](inline-macro.md). If any [block macros](block-macro.md) present in the argument or its descendants, will lead to a conversion error.

Some notable rules:
- [`title` arguments](title-argument.md) are alwayws `inlineOnly`
- all arguments of [inline macros](inline-macro.md) are `inlineOnly`

There are two main rationales for enforcing these rules:
- the HTML `h1` - `h6` header HTML elements can only contain phrasing content (analogout to our [inline macros](inline-macro.md)) for the HTML to be valid. We could chose to use styled `div`s instead of `h` elements, but this could have a negative SEO impact. All other HTML elements could be replaced by `div`s without issue however, the problem really is only `h`.
- on [OurBigBook Web](ourbigbook-web.md), where multiple users are working together and many titles from multiple users show on index pages, it is saner to be more restrictive on what is allowed on titles and to prevent visually very large things from being added in order to prevent bad actors or accidents from disrupting other users too much

## ↑ Ancestors (5)

1. [Macro argument property](macro-argument-property.md)
2. [Macro argument](macro-argument.md)
3. [OurBigBook Markup syntax](ourbigbook-markup-syntax.md)
4. [OurBigBook Markup](ourbigbook-markup.md)
5. [OurBigBook Project](split.md)
