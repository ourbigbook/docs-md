# Header followed by paragraph without blank line does not split correctly

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Bug](bug.md)

<a id="_196"></a>
README.bigb

<a id="_197"></a>
```
= Asdf

== Qwer
zxcv
```

<a id="_198"></a>
then:

<a id="_199"></a>
```
ourbigbook --split-headers README.bigb
```

<a id="_200"></a>
leads to `out/html/split.html` that contains the `Qwer` header, and no `qwer.html` output.

<a id="_201"></a>
This construct should just be forbidden by linting instead forcing the preferred:

<a id="_202"></a>
```
= Asdf

== Qwer

zxcv
```

<a id="_203"></a>
Similar problem with preceding paragraph:

<a id="_204"></a>
README.bigb

<a id="_205"></a>
```
= Asdf

zxcv
== Qwer
```

<a id="_206"></a>
The root failure case in both cases is that the header goes inside the paragraph.

<a id="_207"></a>
Hmm, perhaps that is not a bad behavior... OK so going back a bit further, the problem is the outcome of:<a id="_208"></a>

```
ourbigbook --web .
```
on such cases, which leads to errors.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
