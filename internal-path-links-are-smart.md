# Internal path links are smart

↑ **Parent:** [External link](external-link.md)

When a link is an [internal path link](external-link.md) this has the following effects:
- the correct relative path to the file is used when using nested [scopes](h-scope-argument.md) with [`-S`, `--split-headers`](split-headers.md). For example, if we have:
  ```
  = h1

  == h2
  {scope}

  === h3

  \a[index.js]
  ```
  then in split header mode, `h3` will be rendered to `h2/h3.html`.

  Therefore, if we didn't do anything about it, the link to `index.js` would render as `href="index.js"` and thus point to `h2/index.js` instead of the correct `index.js`.

  Instead, OurBigBook automatically converts it to the correct `href="../index.js"`
- the [`_raw` directory](raw-directory.md) prefix is added to the link
- existence of the file is checked on compilation. If it does not exist, an error is given.

## ↑ Ancestors (7)

1. [External link](external-link.md)
2. [`\a` `external` argument](a-external-argument.md)
3. [`\a` argument](a-argument.md)
4. [Link](link.md)
5. [Macro](macro.md)
6. [OurBigBook Markup](ourbigbook-markup.md)
7. [OurBigBook Project](split.md)
