# Like and unlike requests are very slow

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Performance](performance.md), [Web](web.md)

<a id="_49"></a>
On ourbigbook.com like and unlike takes 4s-10s! Something is wrong. It must be because of the complex side effects like topic updating? Maybe those should be deferred? This only appears noticeable on a larger database.

<a id="_50"></a>
Edit: as of today it was taking 500 ms, so likely some index was added that improved it a lot.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
