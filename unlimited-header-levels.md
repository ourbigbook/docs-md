# Unlimited header levels

↑ **Parent:** [Header](header.md)

There is no limit to how many levels we can have, for either sane or shorthand headers!

HTML is randomly limited to `h6`, so OurBigBook just renders higher levels as an `h6` with a `data-level` attribute to indicate the actual level for possible CSS styling:
```
<h6 data-level="7">My title</h6>
```

The recommended style is to use shorthand headers up to `h6`, and then move to sane one for higher levels though, otherwise it becomes very hard to count the `=` signs.

To avoid this, we considered making the shorthand syntax be instead:
```
= 1 My h1
= 2 My h2
= 3 My h3
```
but it just didn't feel as good, and is a bit harder to type than just smashing `=` n times for lower levels, which is the most common use case. So we just copied markdown.

**Table of contents**

- [My h3](my-h3.md)
  - [My h4](my-h4.md)
    - [My h5](my-h5.md)
      - [My h6](my-h6.md)
        - [My h7](my-h7.md)
          - [My h8](my-h8.md)
            - [My h9](my-h9.md)
              - [My h10](my-h10.md)
                - [My h11](my-h11.md)
                  - [My h12](my-h12.md)
                    - [My h13](my-h13.md)

## ↑ Ancestors (4)

1. [Header](header.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Features](features.md)
- [`\H` `numbered` argument](h-numbered-argument.md)
- [`\H` `parent` argument](h-parent-argument.md)
- [Motivation](motivation.md)
