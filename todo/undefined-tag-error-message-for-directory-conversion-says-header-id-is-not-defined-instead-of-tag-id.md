# Undefined tag error message for directory conversion says header ID is not defined instead of tag ID

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Bug](bug.md), [Tag](tag.md)

<a id="_548"></a>
README.bigb<a id="_549"></a>

```
= Tmp

== Tmp 2
{tag=adsf}
```
convert:<a id="_550"></a>

```
ourbigbook .
```
outcome:<a id="_551"></a>

```
extract_ids: README.bigb
extract_ids: README.bigb finished in 43.47357300110161 ms
error:
README.bigb:4:1: cross reference to unknown id: "tmp-2"
```
expected outcome:<a id="_552"></a>

```
README.bigb:4:1: cross reference to unknown id: "asdf"
```

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
