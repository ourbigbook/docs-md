# The home article

↑ **Parent:** [The toplevel index file](the-toplevel-index-file.md)  
🏷️ **Tags:** [Toplevel header](the-toplevel-header.md)

The "home article" is the first article of [the toplevel index file](the-toplevel-index-file.md). E.g. in:

index.bigb
```
= John Smith's Homepage

== I like dogs
```
then "John Smith's Homepage" is the home article, but "I like dogs" is not.

The home article has some special handling done to it, notably:
- it renders as "Home" in many places as such as the breadcrumb, a way to make things more unified and succinct, especially on web
- it automatically gets two IDs:
  - a main empty ID
  - a [synonym](h-synonym-argument.md) to that empty ID
  For example we could write:
  ```
  = John Smith's Homepage

  == I like dogs

  This is my homepage: <>

  And also: <John Smith's Homepage>
  ```
  Here
  - `<>` renders as "Home"
  - `<John Smith's Homepage>` renders as `John Smith's Homepage`
  but both link to the same location

  As a consequence of the ID being empty, you have to set [`\H` `parent` argument](h-parent-argument.md) of subsequent headers to empty if you witsh to use them as in:
  ```
  = John Smith's Homepage

  = I like dogs
  {parent=}
  ```

  Doing:
  ```
  = John Smith's Homepage

  = I like dogs
  {parent=John Smith's Homepage}
  ```
  doesn't current work because the ID `john-smith-s-homepage` is just a synonym to the empty ID, and you can't currently set `parent=` to point to synonyms:

  This is because the ID John Smith's Homepage

  You can prevent a second ID from being giving by simply setting the ID to be explicitly empty:
  ```
  = John Smith's Homepage
  {id=}
  ```
  which would generte just a single empty ID.

## ↑ Ancestors (5)

1. [The toplevel index file](the-toplevel-index-file.md)
2. [Project toplevel directory](project-toplevel-directory.md)
3. [Index file](index-file.md)
4. [OurBigBook CLI](ourbigbook-cli.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [The ID of the first header is derived from the filename](the-id-of-the-first-header-is-derived-from-the-filename.md)
