# Incoming links and tagged metadata does not show synonyms

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Metadata section](metadata-section.md), [Synonym](synonym.md)

<a id="_53"></a>
Both CLI and web. E.g.:

<a id="_54"></a>
README.bigb<a id="_55"></a>

```
= Index

<notindex2>
```

<a id="_56"></a>
notindex.bigb<a id="_57"></a>

```
= Notindex

= Notindex2
{synonym}
```

<a id="_58"></a>
then:<a id="_59"></a>

```
ourbigbook .
```
the output notindex.html does not have an incoming links metadata section. With `<notindex>` it does have a metadata section. The outcome metadata section should be identical on both.

<a id="_60"></a>
Same for tags that use the synonym.

<a id="_61"></a>
Added a test now for it.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
