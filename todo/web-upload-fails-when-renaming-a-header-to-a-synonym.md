# Web upload fails when renaming a header to a synonym

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web upload](web-upload.md)

<a id="_458"></a>
First:

<a id="_459"></a>
test-data.bigb<a id="_460"></a>

```
= Test data

== Tmp
```
then:<a id="_461"></a>

```
ourbigbook --web-test
```

<a id="_462"></a>
Then modify to:<a id="_463"></a>

```
= Test data

== Tmp2

= Tmp
```
and rerun:<a id="_464"></a>

```
ourbigbook --web-test
```

<a id="_465"></a>
Error message:<a id="_466"></a>

```
param "bodySource" is mandatory when not rendering or when "path" to an existing article is not given. path="tmp"
```

<a id="_467"></a>
Can be worked around by:<a id="_468"></a>

```
rm -rf out
```
therefore it is just a case of some outdated local state, thank God for that, should be simple to fix.

<a id="_469"></a>
The root problem seems to be that `sqlite3 _out/web/web.sqlite3 .dump` still contains `tmp`, we have to get rid of any synonym headers during ID extraction.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
