# Features

↑ **Parent:** [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)

- [internal links](internal-link.md) to any [header](header.md) (including e.g. h2, h3, etc. [in other files](internal-link.md)), [images](image.md), etc. with amazing [error checking and reporting](error-reporting.md): never break [internal links](internal-link.md) without knowing again, and quickly find out what broke when you do. E.g.:

  animal.bigb
  ```
  = Animal

  <Bats> are <flying animals>.
  ```
  Mammal.bigb
  ```
  = Flying animal

  == Bat
  ```
  `Animal.bigb` would render something like:
  ```
  <a href="flying-animal.html#bat">Bats</a> are <a href="flying-animal.html">flying animals</a>.
  ```
  The following would fail and point you out the file and line of the failure:
  - nonexistent id:
    ```
    <Weird animal not documented>
    ```
  - duplicate IDs:
    ```
    = Animal

    == Dog

    == Cat

    == Dog
    ```
- [KaTeX](https://katex.org/) server side [mathematics](mathematics.md), works on browsers with [JavaScript disabled](ourbigbook-web-with-javascript-disabled.md):
  ```
  I like $\sqrt{2}$, but I adore this \x[equation-quadratic-equation]:

  $$
  x^2 + 2x + 1
  $$
  {title=Quadratic equation}
  ```
- multi-file features out of the box so you don't need a separate wrapper like Jekyll to make a multi-page website:
  - [cross file internal links](cross-file-internal-link.md)
  - single-source multi-format output based on [includes](include.md) and build options:
    - by default, one HTML per source with includes rendered as links between pages, e.g.:

      index.bigb
      ```
      = My website

      == h2

      \Include[not-index]
      ```
      not-index.bigb
      ```
      = Not index

      == Not index h2
      ```
      produces `index.html` and `not-index.html`
    - with the [`-S`, `--split-headers`](split-headers.md) option, you can output each header of an input file into a separate output file. The previous filesystem would produce:
      - `index.html`: which contains the full `index.bigb` output
      - `split.html`: split version of the above containing only the `= My website` header and not `h2`
      - `h2.html`: only contains the `h2` header
      - `not-index.html` contains the full output of `not-index.bigb`
      - `not-index-split.html`: only contains the `= Not index` header
      - `not-index-h2.html`: only contains the `= Not index h2` header

      Each of those pages automatically gets a [table of contents](table-of-contents.md)
    - [`--embed-includes`](embed-includes.md) single file output from multiple input files. Includes are parsed smartly, not just source copy pasted, e.g. included headers are shifted from `h1` to `h2` correctly.

      On the previous sample filesystem, it would produce a single output file `index.html` which would contain a header structure like:
      ```
      = My website

      == h2

      === Not index

      ==== Not index h2
      ```
    - supports both local serverless rendering to HTML files for local viewing, and server oriented rendering such as GitHub pages, e.g. [internal links](internal-link.md) automatically get `.html` extension and or not. E.g.:
      - locally, a link `\x[not-index]` would render as `<a href="not-index.html">` and `not-index.bigb` produces `not-index.html`
      - when publishing, `\x[not-index]` would render as `<a  href="not-index">` and `not-index.bigb` also produces `not-index.html`, which the server converts to just `http://my-website.com/not-index`
  - cross file configuration files to factor out common page parts like headers, footers and other metadata, e.g.:
    - `ourbigbook.liquid.html`: [Liquid template](https://github.com/Shopify/liquid) used for all pages, see example at: [Section "Play with the template"](play-with-the-template.md)
    - `main.scss`: CSS stylesheet generated from [SASS](https://sass-lang.com/) input, see example at: [Section "Play with the template"](play-with-the-template.md)
    - `ourbigbook.tex`: global LaTeX math definitions, e.g.:
      ```
      \newcommand{\abs}[1]{\left|#1\right|}
      ```

      and then you can use:
      ```
      $\abs{x}$
      ```

      in any .bigb file of the project.
    - [`ourbigbook.json`](ourbigbook-json.md): per repository configuration options
  - [table of contents](table-of-contents.md) that crosses input files via includes. E.g. in:

    index.bigb
    ```
    = My website

    == h2

    \Include[not-index]
    ```
    not-index.bigb
    ```
    = Not index

    == Not index h2
    ```
    the table of contents for `index.html` also contains the headers for `not-index.bigb` producing:
    - My website
      - h2
        - Not index
          - Not index h2
    This means that you can split large [splitDefault](h-splitdefault-argument.md) input files if rendering starts to slow you down, and things will still render exactly the same.
  - check that local files and images linked to actually exist: [`\a` `external` argument](a-external-argument.md). E.g.:
    ```
    \a[i-don-exist.txt]
    ```

    would lead to a build error.
  - associate headers to files or directories with the [`\H` `file` argument](h-file-argument.md) e.g.:
    ```
    Here's an example of a nice image: \x[path/to/my/image.png]{file}.

    = path/to/my/image.png
    {file}

    This image was taken when I was on vacation!
    ```

    would automatically add a preview of the image on the output. Display files and their metadata nicely directly on your static website rather than relying exclusively on GitHub as a file browser.
- advanced header/ID related features:
  - [ID-based header levels](h-parent-argument.md):
    ```
    = Furry animal

    I like \x[furry-animal]{p}, especially my cat, here is his photo: \x[image-my-cat].

    == Cat

    \Image[My_cat.jpg]
    {title=My cat}
    ```
  - [scopes](h-scope-argument.md) either with directories or with within a single file:
    ```
    See the important conclusion of my experiment: \x[report-of-my-experiment/conclusion]

    = Report of my experiment
    {scope}

    == Introduction

    == Middle

    == Conclusion
    ```
  - [internal link title inflection](internal-link-title-inflection.md) for capitalization and pluralization, e.g.;
    ```
    = Dog

    == Snoopy
    {c}

    \x[dog]{c}{p} are fun. But the \x[dog] I like the most is \x[snoopy]!
    ```

    would render:
    - `\x[dog]{c}{p}` as `Dogs`: capitalized because of `{c}` and pluralized because of `{p}`
    - `\x[dog]` as `dogs`: auto lowercased because its header `= Dog` does not have `{c}`
    - `\x[snoopy]` as `Snoopy`: title capitalization kept to upper case due to `{c}` on the header `== Snoopy`
  - [synonyms](h-synonym-argument.md), e.g.:
    ```
    = User interface

    = UI
    {c}
    {synonym}
    {title2}

    \x[user-interface]{c} is too long, I just say \x[ui].
    ```
    would render something like:
    ```
    <a href="#user-interface">User interface</a> is too long, I just say <a href="user-interface">UI</a>
    ```
    Furthermore, this also generates a output file:
    ```
    ui.html
    ```
    which redirects to the ain `user-interface.html`, so it serves as a way to have backward compatibility on page renames.

    And the `title2` makes it appears on the main title under parenthesis, something like:
    ```
    <h1>User interface (UI)</h1>
    ```
  - [header disambiguation](disambiguate-argument.md), e.g.:
    ```
    My favorite fruits are \x[apple-fruit]{p}!

    My favorite least favorite brand is is \x[apple-company]! \x[apple] computers are too expensive.

    == Apple
    {disambiguate=fruit}

    == Apple
    {c}
    {disambiguate=company}

    = Apple
    {c}
    {synonym}
    ```

    which renders something like:
    - `\x[apple-fruit]{p}`: `<a href="apple-fruit">apples</a>`
    - `\x[apple-company]`: `<a href="apple-company">Apple</a>`
    - `\x[apple]`: also `<a href="apple-company">Apple</a>` because of the synonym
    - `== Apple\n{disambiguate=fruit}`: `<h2 id="apple-fruit">Apple (fruit)</h2>`
    - `== Apple\n{disambiguate=company}`: `<h2 id="apple-company">Apple (company)</h2>`
  - tags are regular headers: [`\H` `child` argument](h-child-argument.md), [`\x` `child` argument](x-child-argument.md)
    ```
    = Animal

    == Dog
    {tag=domestic}
    {tag=cute}

    == Cat
    {tag=domestic}
    {tag=cute}

    == Bat
    {tag=flying}

    = Flying

    = Cute

    = Domestic
    ```
  - [unlimited header levels](unlimited-header-levels.md), levels higher than 6 are rendered in HTML as an appropriately styled `div`s with an ID:
    ```
    = h1

    == h2

    === h3

    ==== h4

    ===== h5

    ====== h6

    ======= h7

    ======== h8
    ```
  - generate lists of [incoming links](incoming-links.md) between internal headers: it shows every [internal link](internal-link.md) coming into the current page
- automatic file upload and directory listing of non OurBigBook files: [`_raw` directory](raw-directory.md), e.g.:
  - link to a file:
    ```
    The file \a[index.js] is cool.
    ```

    which renders as:

    > The file [index.js](index.js) is cool.
  - link to a directory:
    ```
    The directory \a[file_demo] is cooler.
    ```

    which renders as:

    > The directory [file_demo](file_demo) is cooler.
- is written in JavaScript and therefore runs natively on the browser to allow live previews as shown at: [https://docs.ourbigbook.com/_obb/dist/editor](https://docs.ourbigbook.com/_obb/dist/editor)
- helps you with the publishing:
  - [`ourbigbook --publish`](p-publish.md) publishes in a single command to the configured target (default [GitHub Pages](publish-target-github-pages.md))
  - OurBigBook tries to deal with media such as images and video intelligently for you, e.g.: [Section "Where to store images"](where-to-store-images.md). E.g. you can keep media in a separate media repository, `my-media-repository`, and then by configuring on [`ourbigbook.json`](ourbigbook-json.md):
    ```
    "media-providers": {
      "github": {
        "default-for": ["image", "video"],
        "path": "media",
        "remote": "yourname/myproject-media"
      }
    }
    ```

    you can use images in that repository with:
    ```
    \Image[My_image_basename.jpg]
    ```

    instead of:
    ```
    \Image[https://raw.githubusercontent.com/cirosantilli/myproject--media/master/My_image_basename.jpg]
    ```
  - `inotifywait` watch and automatically rebuild with [`-w`, `--watch`](watch.md):
    ```
    ourbigbook --watch input-file.bigb
    ```
- automatic code formatting: [`--format-source`](format-source.md)

## ↑ Ancestors (2)

1. [OurBigBook Markup and CLI overview](ourbigbook-markup-and-cli-overview.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Design goals](design-goals.md)
