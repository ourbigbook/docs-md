<h1 id="raw-directory"><code>_raw</code> directory</h1>

↑ **Parent:** [`\a` `external` argument](a-external-argument.md)

[OurBigBook](split.md) places output files that are not the output of `.bigb` to `.html` conversion (i.e. `.html` output files) under the `_raw/` prefix of the output.

[Internal path links](external-link.md) then automatically add the `_raw/` prefix to every link.

For example, consider an input directory that contains:

notindex.bigb
```
= Hello

Check out \a[myfile.c].

The source code for this file is at: \a[notindex.bigb].

\Image[myimg.png]
```

myfile.c
```
int i = 1;
```

myimg.png
```
Binary!
```

After conversion with:
```
ourbigbook .
```
the following files would exist in the output directory:
- `notindex.html`: converted output of `notindex.bigb`
- `_raw/notindex.bigb`: a copy of the input source code `notindex.bigb`
- `_raw/myfile.c`: a copy of the input file `myfile.c`
- `_raw/myimg.png`: a copy of the input file `myimg.c`
and all links/image references would work and automtically point to the correct locations under `_raw`.

Some live examples:
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

The reason why a `_raw` prefix is needed it to avoid naming conflicts with OurBigBook outputs, e.g. suppose we had the files:
- `configure`
- `configure.bigb`
Then, in a server that omits the `.html` extension, if we didn't have `_raw/` both `configure.html` and `configure` would be present under `/configure`. With `_raw` we instead get:
- `_raw/configure`: the input `/configure` file
- `configure`: the HTML

## 🏷️ Tagged (1)

- [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages.md)

## ↑ Ancestors (6)

1. [`\a` `external` argument](a-external-argument.md)
2. [`\a` argument](a-argument.md)
3. [Link](link.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Features](features.md)
- [`_file` output directory](file-output-directory.md)
- [Internal path links are smart](internal-path-links-are-smart.md)
- [Automatically create `_file` pages for every file](news/automatically-create-file-pages-for-every-file.md)
- [`IgnoreRender`](ourbigbook-json/ignorerender.md)
- [Template variable](template-variable.md)
