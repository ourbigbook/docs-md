# Incoming links and tagged metadata does not show synonyms

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Metadata section](metadata-section.md), [Synonym](synonym.md)

Both CLI and web. E.g.:

README.bigb
```
= Index

<notindex2>
```

notindex.bigb
```
= Notindex

= Notindex2
{synonym}
```

then:
```
ourbigbook .
```
the output notindex.html does not have an incoming links metadata section. With `<notindex>` it does have a metadata section. The outcome metadata section should be identical on both.

Same for tags that use the synonym.

Added a test now for it.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
