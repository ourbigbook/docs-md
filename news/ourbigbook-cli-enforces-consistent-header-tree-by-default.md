# OurBigBook CLI enforces consistent header tree by default

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [OurBigBook CLI](../ourbigbook-cli.md)

<a id="_240"></a>
[OurBigBook CLI](../ourbigbook-cli.md) now forces you to write a consistent tree of headers by default, including e.g.:

<a id="_241"></a>
<a id="_242"></a>
- can't have text under the current header after [Includes](../include.md). E.g. this is not allowed anymore:<a id="_243"></a>

  ```
  = Vertebrate

  Vertebrates are cool.

  \Include[mammal]

  And they have vertebrae.
  ```

  You need instead something like:<a id="_244"></a>

  ```
  = Vertebrate

  Vertebrates are cool.

  And they have vertebrae.

  \Include[mammal]
  ```
<a id="_245"></a>
- files must start with a h1 header and contain only a single h1 header. E.g. in `vertebrate.bigb` this is not allowed because it does not start with a header:<a id="_246"></a>

  ```
  I like vertebrates.

  = Vertebrate
  ```

  Neither is this because it starts with a h2 header:<a id="_247"></a>

  ```
  == Vertebrate

  I like vertebrates.
  ```

  Neither is this because it has two h1 headers:<a id="_248"></a>

  ```
  = Vertebrate

  I like vertebrates.

  = Non-vertebrate

  I don't like non vertebrates.
  ```
<a id="_249"></a>
- <a id="_250"></a>
  prevent infinite [include](../include.md) loop recursion. E.g. this would lead to an infinite loop at render time:

  <a id="_251"></a>
  index.bigb<a id="_252"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

  <a id="_253"></a>
  vertebrate.bigb<a id="_254"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```

  <a id="_255"></a>
  mammal.bigb<a id="_256"></a>

  ```
  = Mammal

  \Include[vertebrate]
  ```

  <a id="_257"></a>
  Now you just get a nice error message instead.
<a id="_258"></a>
- <a id="_259"></a>
  every file must be recursively included from [the toplevel index file](../the-toplevel-index-file.md). E.g.

  <a id="_260"></a>
  index.bigb<a id="_261"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

  <a id="_262"></a>
  vertebrate.bigb<a id="_263"></a>

  ```
  = Vertebrate
  ```

  <a id="_264"></a>
  mammal.bigb<a id="_265"></a>

  ```
  = Mammal
  ```

  <a id="_266"></a>
  would give an error because `mammal.bigb` is not included from anywhere. To fix it you would likely want:

  <a id="_267"></a>
  vertebrate.bigb<a id="_268"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```
<a id="_269"></a>
- <a id="_270"></a>
  files cannot be included twice. Previously the following was allowed:

  <a id="_271"></a>
  index.bigb<a id="_272"></a>

  ```
  = My homepage

  \Include[vertebrate]
  \Include[mammal]
  ```

  <a id="_273"></a>
  vertebrate.bigb<a id="_274"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```

  <a id="_275"></a>
  mammal.bigb<a id="_276"></a>

  ```
  = Mammal
  ```

  <a id="_277"></a>
  But now it gives an error because `mammal.bigb` is included from both `index.bigb` and `vertebrate.bigb`.

  <a id="_278"></a>
  To fix it you would likely instead want to include it only from the most specific location `vertebrate.bigb` and remove it from `index.bigb`:

  <a id="_279"></a>
  index.bigb<a id="_280"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

<a id="_281"></a>
It is a common issue with most plaintext note taking systems that they don't force you to make a consistent tree.

<a id="_282"></a>
However, for publishing, having one tree is essential, otherwise it can be very hard for users to navigate your content.

<a id="_283"></a>
Furthermore, this makes things much simpler to implement and understand for OurBigBook Web and a future WYSIWYG local editor.

<a id="_284"></a>
Some other pedantry:

<a id="_285"></a>
<a id="_286"></a>
- rename `README.bigb` to `index.bigb` for the [the toplevel index file](../the-toplevel-index-file.md). Much cleaner, and we already have a conflict on the baseneme index with index.html, so why create another conflict with README
<a id="_287"></a>
- rename [the `_out` directory](../the-out-directory.md) from `out` to `_out`, which is a reserved ID. Otherwise it was impossible to have a directory called `out` with ourbigbook files for [directory-based `scope`](../directory-based-scope.md).

<a id="_288"></a>
While [OurBigBook Web](../ourbigbook-web.md) topic mind melding remains the most innovative feature of the project, local plaintext is a fundamental guarantee that you will never lose your content, and we intend to keep it awesome.

<a id="_289"></a>
Announcements:<a id="_290"></a>

<a id="_291"></a>
- [https://mastodon.social/@ourbigbook/113549071062984064](https://mastodon.social/@ourbigbook/113549071062984064)
<a id="_292"></a>
- [https://x.com/OurBigBook/status/1861383431973683551](https://x.com/OurBigBook/status/1861383431973683551)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
