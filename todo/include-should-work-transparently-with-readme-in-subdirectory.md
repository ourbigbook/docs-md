# Include should work transparently with README in subdirectory

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Include](include.md), [Web](web.md)

We should be able to write:

animal.bigb
```
= Animal

\Include[dog]
```

dog/README.bigb
```
= Dog
```

since the dog.bigb file should ideally be fully equivalent to

dog.bigb
```
= Dog
{scope}
```

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
