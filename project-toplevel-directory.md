# Project toplevel directory

↑ **Parent:** [Index file](index-file.md)

This directory is determined by first checking the presence of a [`ourbigbook.json`](ourbigbook-json.md) file.

If a [`ourbigbook.json`](ourbigbook-json.md) is found, then the project toplevel directory is the directory that contains that file.
- otherwise, if the input path is a descendant of the current working directory, then the current working directory is used, see also: [the current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)
- otherwise, if the input path is a directory, it is used
- otherwise, the directory containing the input file is used

For example, consider the file following file structure relative to the current working directory:
```
path/to/notindex.bigb
```

In this case:
- if there is no `ourbigbook.json` file:
  - if we run `ourbigbook .`: the toplevel directory is the current directory `.`, and so `notindex.bigb` has ID `path/to/notindex`
  - if we run `ourbigbook path`: same
  - if we run `ourbigbook path/to`: same
  - if we run `ourbigbook path/to/notindex.bigb`: same
- if there is a `path/ourbigbook.json` file:
  - if we run `ourbigbook .`: the toplevel directory is the current directory `.` because the `ourbigbook.json` is below the entry point and is not seen, and so `notindex.bigb` has ID `path/to/notindex`
  - if we run `ourbigbook path`: the toplevel directory is the directory with the `ourbigbook.json`, `path`, and so `notindex.bigb` has ID `to/notindex`
  - if we run `ourbigbook path/to`: same
  - if we run `ourbigbook path/to/notindex.bigb`: same

**Table of contents**

- [The toplevel index file](the-toplevel-index-file.md)
  - [The home article](the-home-article.md)
  - [The current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)

## ↑ Ancestors (3)

1. [Index file](index-file.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (8)

- [Git tracked project](git-tracked-project.md)
- [Index file](index-file.md)
- [`Ignore`](ourbigbook-json/ignore.md)
- [`--outdir <outdir>`](outdir.md)
- [Template variable](template-variable.md)
- [The current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)
- [The toplevel index file](the-toplevel-index-file.md)
- [Visual Studio Code documentation](visual-studio-code-documentation.md)
