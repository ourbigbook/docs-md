# Header followed by paragraph without blank line does not split correctly

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Bug](bug.md)

README.bigb

```
= Asdf

== Qwer
zxcv
```

then:

```
ourbigbook --split-headers README.bigb
```

leads to `out/html/split.html` that contains the `Qwer` header, and no `qwer.html` output.

This construct should just be forbidden by linting instead forcing the preferred:

```
= Asdf

== Qwer

zxcv
```

Similar problem with preceding paragraph:

README.bigb

```
= Asdf

zxcv
== Qwer
```

The root failure case in both cases is that the header goes inside the paragraph.

Hmm, perhaps that is not a bad behavior... OK so going back a bit further, the problem is the outcome of:
```
ourbigbook --web .
```
on such cases, which leads to errors.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
