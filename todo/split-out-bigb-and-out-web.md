<h1 id="split-out-bigb-and-out-web">Split _out/bigb and _out/web</h1>

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Bug](bug.md)

<a id="_581"></a>
Currently:<a id="_582"></a>

```
ourbigbook --web
```
stores the split renders under:<a id="_583"></a>

```
out/bigb
```
since it is a bigb output.

<a id="_584"></a>
However, that bigb output is different from the one gnerated with:<a id="_585"></a>

```
ourbigbook -O bigb .
```
since the latter contains `\Include` which need to be removed from the `web/` output.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
