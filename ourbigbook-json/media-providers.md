<h1 id="ourbigbook-json/media-providers"><code>media-providers</code></h1>

↑ **Parent:** [`Ourbigbook.json`](../ourbigbook-json.md)

<a id="ourbigbook-json/_3843"></a>
The `media-providers` entry of `ourbigbook.json` specifies properties of how media such as [images](../image.md) and [videos](../video.md) are retrieved and rendered.

<a id="ourbigbook-json/_3844"></a>
The general format of `media-providers` looks like:<a id="ourbigbook-json/_3845"></a>

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

<a id="ourbigbook-json/_3846"></a>
Properties that are valid for every provider:<a id="ourbigbook-json/_3847"></a>

<a id="ourbigbook-json/_3848"></a>
- <a id="ourbigbook-json/_3849"></a>
  `default-for`: use this provider as the default for the given types of listed macros.

  <a id="ourbigbook-json/_3850"></a>
  The first character of the macros are case insensitive and must be given as lower case. Therefore e.g.:<a id="ourbigbook-json/_3851"></a>

  <a id="ourbigbook-json/_3852"></a>
  - `image` applies to both `image` and `Image`
  <a id="ourbigbook-json/_3853"></a>
  - giving `Image` is an error because that starts with an upper case character
<a id="ourbigbook-json/_3854"></a>
- `title-from-src` (`bool`): extract the `title` argument from the `src` by default for media such as [images](../image.md) and [videos](../video.md) as if the `titleFromSrc` macro argument had been given, see also: [Section "Image ID"](../image-id.md)

<a id="ourbigbook-json/_3855"></a>
Direct children of media-providers and subproperties that are valid only for them specifically:<a id="ourbigbook-json/_3856"></a>

<a id="ourbigbook-json/_3857"></a>
- `local`: tracked in the current Git repository as mentioned at [Section "Store images inside the repository itself"](../store-images-inside-the-repository-itself.md)<a id="ourbigbook-json/_3858"></a>

  <a id="ourbigbook-json/_3859"></a>
  - `path`: location of the cloned local repository relative to the root the main repository
<a id="ourbigbook-json/_3860"></a>
- `github`: tracked in a separate Git repository as mentioned at [Section "Store images in a separate media repository"](../store-images-in-a-separate-media-repository.md)<a id="ourbigbook-json/_3861"></a>

  <a id="ourbigbook-json/_3862"></a>
  - <a id="ourbigbook-json/_3863"></a>
    `path`: analogous to `path` for `local`: a local location for this GitHub provider, where the repository can optionally be cloned.

    <a id="ourbigbook-json/_3864"></a>
    When not during a run with the [`--publish` option](../p-publish.md), OurBigBook checks if the path exists locally, and if it does, then it uses that local directory as the source intead of the GitHub repository.

    <a id="ourbigbook-json/_3865"></a>
    This allows you to develop locally without Internet and see the latest version of the images without pushing them.

    <a id="ourbigbook-json/_3866"></a>
    During publishing, the GitHub version is used instead.

    <a id="ourbigbook-json/_3867"></a>
    TODO make this even more awesome by finishing to implement [https://github.com/ourbigbook/ourbigbook/issues/184](https://github.com/ourbigbook/ourbigbook/issues/184):<a id="ourbigbook-json/_3868"></a>

    <a id="ourbigbook-json/_3869"></a>
    - automatically `git push` this repository during deployment to ensure that any asset changes will be available.
    <a id="ourbigbook-json/_3870"></a>
    - <a id="ourbigbook-json/_3871"></a>
      ignore the path from OurBigBook conversion as if added to [`ignore`](ignore.md), and is not added to the final output, because you are already going to have a copy of it.

      <a id="ourbigbook-json/_3872"></a>
      This way you can use the sanes approach which is to track the directory as a Git submodule as mentioned at: [store images in a separate media repository and track it as a git submodule](../store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md), instead of either:<a id="ourbigbook-json/_3873"></a>

      <a id="ourbigbook-json/_3874"></a>
      - keeping it outside of the repository
      <a id="ourbigbook-json/_3875"></a>
      - keeping it in the repository but explicitly ignoring it as well, which is a bit redundant
  <a id="ourbigbook-json/_3876"></a>
  - `remote`: `<github-username>/<repo-name>`
<a id="ourbigbook-json/_3877"></a>
- `youtube`: YouTube [videos](../video.md)

<a id="ourbigbook-json/_3878"></a>
See also: [https://github.com/ourbigbook/ourbigbook/issues/40](https://github.com/ourbigbook/ourbigbook/issues/40)

## ↑ Ancestors (3)

1. [`Ourbigbook.json`](../ourbigbook-json.md)
2. [OurBigBook CLI](../ourbigbook-cli.md)
3. [OurBigBook Project](../split.md)

## ← Incoming links (7)

- [`Disambiguate` argument](../disambiguate-argument.md)
- [`--embed-resources`](../embed-resources.md)
- [Image ID](../image-id.md)
- [Store images in a separate media repository](../store-images-in-a-separate-media-repository.md)
- [Store images in a separate media repository and track it as a git submodule](../store-images-in-a-separate-media-repository-and-track-it-as-a-git-submodule.md)
- [Store images in Wikimedia Commons](../store-images-in-wikimedia-commons.md)
- [Template variable](../template-variable.md)
