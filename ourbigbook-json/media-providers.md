<h1 id="ourbigbook-json/media-providers"><code>media-providers</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

The `media-providers` entry of `ourbigbook.json` specifies properties of how media such as [images](../image.md) and [videos](../video.md) are retrieved and rendered.

The general format of `media-providers` looks like:
```
"media-providers": {
  "github": {
    "default-for": ["image"], // "all" to default for both image, video and anything else
    "path": "data/media/",    // data is gitignored, but should not be nuked like _out/
    "remote": "ourbigbook/ourbigbook-media"
  },
  "local": {
    "default-for": ["video"],
    "path": "media/",
  },
  "youtube": {}
}
```

Properties that are valid for every provider:
- `default-for`: use this provider as the default for the given types of listed macros.

  The first character of the macros are case insensitive and must be given as lower case. Therefore e.g.:
  - `image` applies to both `image` and `Image`
  - giving `Image` is an error because that starts with an upper case character
- `title-from-src` (`bool`): extract the `title` argument from the `src` by default for media such as [images](../image.md) and [videos](../video.md) as if the `titleFromSrc` macro argument had been given, see also: [Section "Image ID"](../image-id.md)

Direct children of media-providers and subproperties that are valid only for them specifically:
- `local`: tracked in the current Git repository as mentioned at [Section "Store images inside the repository itself"](../store-images-inside-the-repository-itself.md)
  - `path`: location of the cloned local repository relative to the root the main repository

    For example, set `"local": {"path": "-/media"}` to keep media in a separate repository or Git submodule under `-/media`. Relative image and video paths mirror the source file's directory inside the media directory: `\Image[diagram.svg]` in `subdir/paper.bigb` selects `-/media/subdir/diagram.svg`, and `\Image[../shared.svg]` selects `-/media/shared.svg`. A leading `/` explicitly selects the provider root: `\Image[/diagram.svg]` selects `-/media/diagram.svg`. For compatibility, an unprefixed path also falls back to the provider root if the source-relative file does not exist there. Without `path`, media paths remain relative to the source file.

    Normal source conversion skips `-/` directories and the configured media directory, without needing an explicit `ignoreConvert` entry. Running `ourbigbook .` at the project root also walks the media directory, even when it is outside the project (for example `../wiki-media`). Its files appear at the logical site root in `-/dir` listings, with automatic `-/file` previews unless an explicit file page already exists, and copies under `-/raw`. Media repository `.bigb` and `.md` files are treated as files to preview, not articles to convert. Git metadata and Git-ignored files are excluded. Local image and video renders still reference the media files directly.

    When publishing to GitHub, the media directory must be its own Git repository with a GitHub `origin`: OurBigBook pushes its current commit and merges its committed files into the generated site's root directory, preserving their relative paths. Images and videos use relative links on the site's own domain, without a Git commit SHA in their URLs. Git metadata is excluded, and collisions with generated files and symbolic links are rejected. Commit media changes before publishing; `--dry-run` and `--dry-run-push` suppress the push but still copy the media into the local publish output.

    With `--web`, files from the media directory are merged into your upload root, preserving their paths without an extra `media/` prefix. Image and video references are rewritten automatically, preserving source-relative paths even when scoped headers become separate articles. Git-ignored files and Git metadata are excluded; unchanged files are skipped by hash. Collisions with source-repository files or directories abort before any files are uploaded or unlisted.
- `github`: tracked in a separate Git repository as mentioned at [Section "Store images in a separate media repository"](../store-images-in-a-separate-media-repository.md)
  - `path`: analogous to `path` for `local`: a local location for this GitHub provider, where the repository can optionally be cloned.

    When not during a run with the [`--publish` option](../p-publish.md), OurBigBook checks if the path exists locally, and if it does, then it uses that local directory as the source intead of the GitHub repository.

    This allows you to develop locally without Internet and see the latest version of the images without pushing them.

    During publishing, the GitHub version is used instead.

    TODO make this even more awesome by finishing to implement [https://github.com/ourbigbook/ourbigbook/issues/184](https://github.com/ourbigbook/ourbigbook/issues/184):
    - automatically `git push` this repository during deployment to ensure that any asset changes will be available.
    - ignore the path from OurBigBook conversion as if added to [`ignore`](ignore.md), and is not added to the final output, because you are already going to have a copy of it.

      This way you can use the sanes approach which is to track the directory as a Git submodule as mentioned at: [store images in a separate media repository and track it as a git submodule](../store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md), instead of either:
      - keeping it outside of the repository
      - keeping it in the repository but explicitly ignoring it as well, which is a bit redundant
  - `remote`: `<github-username>/<repo-name>`
- `youtube`: YouTube [videos](../video.md)

See also: [https://github.com/ourbigbook/ourbigbook/issues/40](https://github.com/ourbigbook/ourbigbook/issues/40)

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (8)

- [`Disambiguate` argument](../disambiguate-argument.md)
- [`--embed-resources`](../embed-resources.md)
- [Image ID](../image-id.md)
- [`IgnoreConvert`](ignoreconvert.md)
- [Store images in a separate media repository](../store-images-in-a-separate-media-repository.md)
- [Store images in a separate media repository and track it as a git submodule](../store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md)
- [Store images in Wikimedia Commons](../store-images-in-wikimedia-commons.md)
- [Template variable](../template-variable.md)
