<h1 id="split-out-bigb-and-out-web">Split _out/bigb and _out/web</h1>

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Bug](bug.md)

Currently:
```
ourbigbook --web
```
stores the split renders under:
```
out/bigb
```
since it is a bigb output.

However, that bigb output is different from the one gnerated with:
```
ourbigbook -O bigb .
```
since the latter contains `\Include` which need to be removed from the `web/` output.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
