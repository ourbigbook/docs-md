# Include should work transparently with README in subdirectory

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Include](include.md), [Web](web.md)

<a id="_274"></a>
We should be able to write:

<a id="_275"></a>
animal.bigb<a id="_276"></a>

```
= Animal

\Include[dog]
```

<a id="_277"></a>
dog/README.bigb<a id="_278"></a>

```
= Dog
```

<a id="_279"></a>
since the dog.bigb file should ideally be fully equivalent to

<a id="_280"></a>
dog.bigb<a id="_281"></a>

```
= Dog
{scope}
```

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
