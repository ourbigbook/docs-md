<h1 id="ref-file-normalization">Id, Ref and File foreign normalization</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [DB](db.md)

<a id="_91"></a>
We've started noticing this as we went along and became more familiar with proper database design:<a id="_92"></a>

<a id="_93"></a>
- Ref.from\_id and to\_id should point to Id
<a id="_94"></a>
- File should be removed when deleted: [https://github.com/ourbigbook/ourbigbook/issues/216](https://github.com/ourbigbook/ourbigbook/issues/216) Currently this can only happen locally. Edit: will also start happening on upstream with synonym moves.
<a id="_95"></a>
- toplevel\_id<a id="_96"></a>

  <a id="_97"></a>
  - File.toplevel\_id should point to an Id object via primary key. Currently done via idid text.
  <a id="_98"></a>
  - Id.toplevel\_id should point to an Id object. No links at all apparently.
<a id="_99"></a>
- Article.topicId should point to Topic.id, not be TEXT

<a id="_100"></a>
We could then consider removing several `Ref.destroy` and `Id.destroy` `ON CASCADE` with `File` and `Id`, rather than manually.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
