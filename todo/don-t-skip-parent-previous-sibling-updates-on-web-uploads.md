<h1 id="don-t-skip-parent-previous-sibling-updates-on-web-uploads">Don't skip parent/previous sibling updates on --web uploads</h1>

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web](web.md), [Web upload](web-upload.md)

<a id="_499"></a>
We have recently implemented SHA-256 skips when article content hasn't changed.

<a id="_500"></a>
But we also need to check if the parent or previous sibling has changed, and if it has then update that.

<a id="_501"></a>
We could just return parent and previous sibling on the `/hash` endpoint.

<a id="_502"></a>
Or we need to add that information to the SHA.

<a id="_503"></a>
Ideally we should also have a way to change the tree without re-render, though we could start with re-render for simplicity.

<a id="_504"></a>
This actually breaks uploads because it leads to inconsistencies when finding previousSiblingId.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
