# Ordered list lost when rendering to bigb output format

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [`Bigb` output format](../bigb-output-format.md)

<a id="_436"></a>
Added a commented out test to [test_bigb_output.bigb](test_bigb_output.bigb):<a id="_437"></a>

```
\Ol[
* p1
* p2
]
```
renders to just:<a id="_438"></a>

```
* p1
* p2
```
Also it might be possible to get an extra newline due to this which breaks web upload, but we don't have a min repro currently.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
