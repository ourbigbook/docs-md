# OurBigBook CLI enforces consistent header tree by default

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [OurBigBook CLI](../ourbigbook-cli.md)

[OurBigBook CLI](../ourbigbook-cli.md) now forces you to write a consistent tree of headers by default, including e.g.:

- can't have text under the current header after [Includes](../include.md). E.g. this is not allowed anymore:
  ```
  = Vertebrate

  Vertebrates are cool.

  \Include[mammal]

  And they have vertebrae.
  ```

  You need instead something like:
  ```
  = Vertebrate

  Vertebrates are cool.

  And they have vertebrae.

  \Include[mammal]
  ```
- files must start with a h1 header and contain only a single h1 header. E.g. in `vertebrate.bigb` this is not allowed because it does not start with a header:
  ```
  I like vertebrates.

  = Vertebrate
  ```

  Neither is this because it starts with a h2 header:
  ```
  == Vertebrate

  I like vertebrates.
  ```

  Neither is this because it has two h1 headers:
  ```
  = Vertebrate

  I like vertebrates.

  = Non-vertebrate

  I don't like non vertebrates.
  ```
- prevent infinite [include](../include.md) loop recursion. E.g. this would lead to an infinite loop at render time:

  index.bigb
  ```
  = My homepage

  \Include[vertebrate]
  ```

  vertebrate.bigb
  ```
  = Vertebrate

  \Include[mammal]
  ```

  mammal.bigb
  ```
  = Mammal

  \Include[vertebrate]
  ```

  Now you just get a nice error message instead.
- every file must be recursively included from [the toplevel index file](../the-toplevel-index-file.md). E.g.

  index.bigb
  ```
  = My homepage

  \Include[vertebrate]
  ```

  vertebrate.bigb
  ```
  = Vertebrate
  ```

  mammal.bigb
  ```
  = Mammal
  ```

  would give an error because `mammal.bigb` is not included from anywhere. To fix it you would likely want:

  vertebrate.bigb
  ```
  = Vertebrate

  \Include[mammal]
  ```
- files cannot be included twice. Previously the following was allowed:

  index.bigb
  ```
  = My homepage

  \Include[vertebrate]
  \Include[mammal]
  ```

  vertebrate.bigb
  ```
  = Vertebrate

  \Include[mammal]
  ```

  mammal.bigb
  ```
  = Mammal
  ```

  But now it gives an error because `mammal.bigb` is included from both `index.bigb` and `vertebrate.bigb`.

  To fix it you would likely instead want to include it only from the most specific location `vertebrate.bigb` and remove it from `index.bigb`:

  index.bigb
  ```
  = My homepage

  \Include[vertebrate]
  ```

It is a common issue with most plaintext note taking systems that they don't force you to make a consistent tree.

However, for publishing, having one tree is essential, otherwise it can be very hard for users to navigate your content.

Furthermore, this makes things much simpler to implement and understand for OurBigBook Web and a future WYSIWYG local editor.

Some other pedantry:

- rename `README.bigb` to `index.bigb` for the [the toplevel index file](../the-toplevel-index-file.md). Much cleaner, and we already have a conflict on the baseneme index with index.html, so why create another conflict with README
- rename [the `_out` directory](../the-out-directory.md) from `out` to `_out`, which is a reserved ID. Otherwise it was impossible to have a directory called `out` with ourbigbook files for [directory-based `scope`](../directory-based-scope.md).

While [OurBigBook Web](../ourbigbook-web.md) topic mind melding remains the most innovative feature of the project, local plaintext is a fundamental guarantee that you will never lose your content, and we intend to keep it awesome.

Announcements:
- [https://mastodon.social/@ourbigbook/113549071062984064](https://mastodon.social/@ourbigbook/113549071062984064)
- [https://x.com/OurBigBook/status/1861383431973683551](https://x.com/OurBigBook/status/1861383431973683551)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
