# `\Include` from subdirectories

↑ **Parent:** [Include](include.md)

When you are in a subdirectory, include resolution just is simply relative to the subdirectory. E.g. we could do:

subdir/index.bigb
```
= Subdir

\Include[notindex]
\Include[subdir2/notindex]
```

subdir/notindex.bigb
```
= Notindex
```

subdir/subdir2/notindex.bigb
```
= Notindex
```

It is not currently possible to include from ancestor directories: [https://github.com/ourbigbook/ourbigbook/issues/214](https://github.com/ourbigbook/ourbigbook/issues/214).

## ↑ Ancestors (4)

1. [Include](include.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
