# Store images in a separate media repository and track it as a git submodule

↑ **Parent:** [Store images in a separate media repository](store-images-in-a-separate-media-repository.md)

This is likely the sanest approach possible, as it clearly specifies which media version matches which repository version through the submodule link.

Furthermore, it is possible to make the submodule clone completely optional by setting things up as follows. For your OurBigBook project `yourname/myproject` create a  `yourname/myproject-media` with the media, and track it as a submodule under `yourname/myproject/media`.

Then, add to [`media-providers`](ourbigbook-json/media-providers.md):
```
"media-providers": {
  "github": {
    "default-for": ["image", "video"],
    "path": "media",
    "remote": "yourname/myproject-media"
  }
}
```

Now, as mentioned at [`media-providers`](ourbigbook-json/media-providers.md), everything will work beautifully:

- `ourbigbook .` local conversion will use images from `media/` if it exists, e.g.:
  ```
  \Image[myimage.jpg]
  ```
  will render `media/myimage.jpg`. So after cloning the submodule, you will be able to see the images on the rendered pages without an internet connection.

  But if the submodule is not cloned, not problem, renders will detect that and automatically use GitHub images.

  Then, when you do:
  ```
  ourbigbook --publish
  ```
  the following happen:
  - `\Image[myimage.jpg]` uses the GitHub URL
  - automatically push `media/` to GitHub in case there were any updates
  - also, that directory is automatically gitignore, so it won't be pushed as part of the main render and thus duplicate things

## ↑ Ancestors (6)

1. [Store images in a separate media repository](store-images-in-a-separate-media-repository.md)
2. [Where to store images](where-to-store-images.md)
3. [Image](image.md)
4. [Macro](macro.md)
5. [OurBigBook Markup](ourbigbook-markup.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [`Media-providers`](ourbigbook-json/media-providers.md)
- [Store images inside the repository itself](store-images-inside-the-repository-itself.md)
