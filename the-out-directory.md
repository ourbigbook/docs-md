<h1 id="the-out-directory">The <code>_out</code> directory</h1>

↑ **Parent:** [Overview of files in this repository](overview-of-files-in-this-repository.md)

OurBigBook stores some metadata and outputs it generates/needs inside the `./_out/` directory that it creates inside the [`--outdir <outdir>`](outdir.md).

Overview of files it contains:
- `db.sqlite3`: [cross file internal link internals](cross-file-internal-link-internals.md)
- `publish`: a git clone of the source of the main repository to ensure that untracked files won't accidentally go into the output
  - `publish/_out/db.sqlite3`: like `_out/db.sqlite3` but from the clean clone of `_out/publish`
  - `publish/_out/publish`: the final generated output directory that gets published, e.g. as in [publish to GitHub Pages](publish-target-github-pages.md)

## ↑ Ancestors (3)

1. [Overview of files in this repository](overview-of-files-in-this-repository.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (7)

- [Cross file internal link internals](cross-file-internal-link-internals.md)
- [`--dry-run`](dry-run.md)
- [Ignored files](ignored-files.md)
- [OurBigBook CLI enforces consistent header tree by default](news/ourbigbook-cli-enforces-consistent-header-tree-by-default.md)
- [`OutputOutOfTree`](ourbigbook-json/outputoutoftree.md)
- [`--outdir <outdir>`](outdir.md)
- [The current working directory does not matter when there is a `ourbigbook.json`](the-current-working-directory-does-not-matter-when-there-is-a-ourbigbook-json.md)
