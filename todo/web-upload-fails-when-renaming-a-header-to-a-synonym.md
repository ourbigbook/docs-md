# Web upload fails when renaming a header to a synonym

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web upload](web-upload.md)

First:

test-data.bigb
```
= Test data

== Tmp
```
then:
```
ourbigbook --web-test
```

Then modify to:
```
= Test data

== Tmp2

= Tmp
```
and rerun:
```
ourbigbook --web-test
```

Error message:
```
param "bodySource" is mandatory when not rendering or when "path" to an existing article is not given. path="tmp"
```

Can be worked around by:
```
rm -rf out
```
therefore it is just a case of some outdated local state, thank God for that, should be simple to fix.

The root problem seems to be that `sqlite3 _out/web/web.sqlite3 .dump` still contains `tmp`, we have to get rid of any synonym headers during ID extraction.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
