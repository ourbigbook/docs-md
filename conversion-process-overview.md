# Conversion process overview

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

A conversion follows the following steps done for each file to be converted:
- tokenizer. Reads the input and converts it to a linear list of tokens.
- parser. Reads the list of tokens and converts it into an [abstract syntax tree](abstract-syntax-tree.md). Parse can be called multiple times recursively when doing things like.
- ast post process pass 1.

  An ast post process pass takes abstract syntax tree that comes out of a previous step, e.g. the original parser output, and modifies the it tree to achieve various different functionalities.

  We may need iterate the tree multiple times to achieve all desired effects, at the time of writing it was done twice. Each iteration is called pass.

  You can view snapshots of the tree after each pass with the [`--log`](log.md) option:
  ```
  ourbigbook --log=ast-pp-simple input.bigb
  ```

  This first pass basically does few but very wide reacing operations that will determine what data we will have to fetch from the database during the followng DB queries step.

  It might also do some operations that are required for pass 2 but that don't necessarily fetch data, not sure anymore.

  E.g. this is where the following functionality are implemented:
  - [synonym](h-synonym-argument.md) and [scope](h-scope-argument.md)
  - [`\OurBigBookExample`](ourbigbookexample.md) and [`--embed-includes`](embed-includes.md): they are stitched into the main AST
- ast post process pass 2: we now do every other post process operation that was not done in pass 1, e.g.:
  - [shorthand](macro-shorthand-syntax.md) paragraphs, lists and tables
- ast post process pass 3: this does some minimal tree hierarchy linking between parents and children. TODO could it be merged into 2? Feels likely
- render, which converts our AST tree into a output string. This is run once for the toplevel, and once for every header of the document if [`-S`, `--split-headers`](split-headers.md) are enabled. We need to do this because header renders are different from their toplevel counterparts, e.g. their first paragraph has id `p-1` and not `p-283`. All of those renders are done from the same parsed tree however, parsing happens only once.

  This step is skipped when using the [`--no-render`](no-render.md) option, or during [ID extraction](id-extraction.md).

  TODO it is intended that it should not be possible for there to be rendering errors once the previous steps have concluded successfully. This is currently not the case for at least one known scenario however: [internal links](internal-link.md) that are not defined.

  Sub-steps include:
  - DB queries: this is the first thing we do during the rendering step.

    Every single database query must be done at this point, in one go.

    Database queries are only done while rendering, never when parsing. The database is nothing but a cache for source file state, and this separation means that we can always cache input source state into the database during parsing without relying on the database itself, and thus preventing any circular dependencies from parsing to parsing.[https://cirosantilli.com/china-dictatorship/reddit](https://cirosantilli.com/china-dictatorship/reddit)

    Keeping all queries together is fundamental for performance reasons, especially of [browser editor with preview](browser-editor-with-preview.md) in the [OurBigBook Web](ourbigbook-web.md): imagine doing 100 scattered server queries:
    ```
    SELECT * from Ids WHERE id = '0'
    SELECT * from Ids WHERE id = '1'
    ...
    SELECT * from Ids WHERE id = '100'
    ```
    vs grouping them together:
    ```
    SELECT * from Ids WHERE id IN ('0', '1', ..., '100')
    ```
    It also has the benefit of allowing us to remove `async`/`await` from almost every single function in the code, which considerably slows down the CPU-bound execution path.

    As an added bonus, it also allows us to clearly see the impact of database queries when using [`--log perf`](log-perf.md).

    We call this joining up of small queries into big ones "query bundling".
- at the every end of the conversion, we then save the database changes calculated during parsing and post processing back to the DB so that the conversion of other files will pick them up.

  Just like for the SELECT, we do a single large INSERT/UPDATE query per database to reduce the round trips.

Conversion of a directory with multiple input files works as follows:
- do one [ID extraction](id-extraction.md) pass without render
- do a global database check/fixup for all files that have been parsed which checks in one go for:
  - check that all [internal link](internal-link.md) targets exist.

    When using the [`\x` `magic` argument](x-magic-argument.md):
    - only one of the plural/singular needs to exist
    - we then decide which one to use and delete the other one. Both are initially placed in the database during the [ID extraction](id-extraction.md) phase.
  - duplicate IDs
  - references from one non-header title to another non-header title as mentioned at [`\x` within `title` restrictions](x-within-title-restrictions.md)

  Ideally, failure of any of the above checks should lead to the database not being updated with new values, but that is not the case as of writing.
- do one conversion pass with render. To speed up conversion, we might at some point start storing a parsed JSON after the first conversion pass, and then just deserialize it and convert the deserialized output directly without re-parsing.
The two pass approach is required to resolve [internal links](internal-link.md)

**Table of contents**

- [ID extraction](id-extraction.md)
- [Abstract syntax tree](abstract-syntax-tree.md)
- [Autogenerated tests](autogenerated-tests.md)
  - [generate-paragraphs](generate-paragraphs.md)

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [-`F`, `--force-render`](force-render.md)
- [`--log`](log.md)
- [`--log perf`](log-perf.md)
