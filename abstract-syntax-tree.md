# Abstract syntax tree

↑ **Parent:** [Conversion process overview](conversion-process-overview.md)

The implementation of much of the functionality of OurBigBook involves manipulating the abstract syntax tree.

The structure of the AST is as follows:
- `AstNode`: contains a map from argument names to the values of each argument, which are of type AstArgument
- `AstArgument`: contains a list of `AstNode`. These are generally just joined up on the output, one after the other.

  One important exception to this are plaintext nodes. These nodes contain just raw strings instead of a list of arguments. They are usually the leaf nodes.

We can easily observe the AST of an input document by using the [`--log`](log.md) following log options:
```
ourbigbook --log=ast-simple input.bigb
ourbigbook --log=ast input.bigb
```

For example, the document:
```
= My title
{c}

A link to \x[another-title]{c}{p} and more text.

== Another title
```
produces with `--log=ast-simple` the following output:
```
ast Toplevel
  arg content
    ast H id="tmp"
      arg c
      arg level
        ast plaintext "1"
      arg numbered
        ast plaintext "0"
      arg scope
        ast plaintext "0"
      arg splitDefault
        ast plaintext "0"
      arg synonym
        ast plaintext "0"
      arg title
        ast plaintext "My title"
    ast P id="p-1"
      arg content
        ast plaintext "A link to "
        ast x
          arg c
          arg child
            ast plaintext "0"
          arg full
            ast plaintext "0"
          arg href
            ast plaintext "another-title"
          arg p
          arg parent
            ast plaintext "0"
          arg ref
            ast plaintext "0"
        ast plaintext " and more text."
    ast Toc id="toc"
    ast H id="another-title"
      arg c
        ast plaintext "0"
      arg level
        ast plaintext "2"
      arg numbered
        ast plaintext "0"
      arg scope
        ast plaintext "0"
      arg splitDefault
        ast plaintext "0"
      arg synonym
        ast plaintext "0"
      arg title
        ast plaintext "Another title"
```

## ↑ Ancestors (3)

1. [Conversion process overview](conversion-process-overview.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (4)

- [Conversion process overview](conversion-process-overview.md)
- [`Lib:` vs `cli:` tests](lib-vs-cli-tests.md)
- [`--log`](log.md)
- [`Multiple` argument](multiple-argument.md)
