<h1 id="ref-file-normalization">Id, Ref and File foreign normalization</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [DB](db.md)

We've started noticing this as we went along and became more familiar with proper database design:
- Ref.from\_id and to\_id should point to Id
- File should be removed when deleted: [https://github.com/ourbigbook/ourbigbook/issues/216](https://github.com/ourbigbook/ourbigbook/issues/216) Currently this can only happen locally. Edit: will also start happening on upstream with synonym moves.
- toplevel\_id
  - File.toplevel\_id should point to an Id object via primary key. Currently done via idid text.
  - Id.toplevel\_id should point to an Id object. No links at all apparently.
- Article.topicId should point to Topic.id, not be TEXT

We could then consider removing several `Ref.destroy` and `Id.destroy` `ON CASCADE` with `File` and `Id`, rather than manually.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
