# Allow creating new pages under scope on web

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Scope](scope.md), [Web](web.md)

<a id="_406"></a>
This casually started working without us noticing much after 3f4e7594ea5d28c3b30a0b7e874ca4627849cbea made parent selection a bit more accurate for scopes. Hurray.

<a id="_407"></a>
We likely just have to set the `path:` API argument based on the has scope status of the parent article.

<a id="_408"></a>
As of the commit that adds this line, it should likely be possible to do it on the backend. On the frontend however we convert `/` to `-` so it doesn't work on the existence checks. We need a more accurate ID conversion there.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
