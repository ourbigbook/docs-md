# Shorthand topic links with a single word

↑ **Parent:** [Shorthand topic link](shorthand-topic-link.md)  
🏷️ **Tags:** [Shorthand macro syntax](macro-shorthand-syntax.md)

If an [shorthand topic link](shorthand-topic-link.md) is made up of a single word then it can be written in the following even succincter notation, without the need for angle brackets:
```
I like #dogs
```
which renders as:



> I like [dogs](https://ourbigbook.com/go/topic/dogs)

is equivalent to:
```
I like <#dogs>
```

Word separation is defined analogously to [shorthand link parsing rules](shorthand-link-parsing-rules.md), i.e.:
- `#` can start from anywhere, including the middle of words, e.g.:
  ```
  abc#mytopic
  ```

  which renders as:

  > abc[mytopic](https://ourbigbook.com/go/topic/mytopic)

  would produce a link immediately preceded by the characters `abc`.
- `#` ends at any [shorthand link termination character](shorthand-link-termination-character.md), e.g.:
  - Topic is `mytopic`:
    ```
    #mytopic is cool
    ```

    which renders as:

    > [mytopic](https://ourbigbook.com/go/topic/mytopic) is cool
  - Topic is `mytopic,` with the comma:
    ```
    #mytopic, is cool
    ```

    which renders as:

    > [mytopic,](https://ourbigbook.com/go/topic/mytopic) is cool

    So you likely would have had instead used the sane syntax in this case with `<#mytopic>, is cool` to avoid that.

## ↑ Ancestors (7)

1. [Shorthand topic link](shorthand-topic-link.md)
2. [`\x` `topic` argument](x-topic-argument.md)
3. [`\x` arguments](x-arguments.md)
4. [Internal link](internal-link.md)
5. [Macro](macro.md)
6. [OurBigBook Markup](ourbigbook-markup.md)
7. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Shorthand link termination character](shorthand-link-termination-character.md)
- [History of Tiananmen Square](wiki-explicit-subsection.md)
