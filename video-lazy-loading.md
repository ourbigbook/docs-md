# Video lazy loading

↑ **Parent:** [Video](video.md)

Unlike [image lazy loading](image-lazy-loading.md), we don't support video lazy loading yet because:
- non-`youtube` videos use the `video` tag which has no `loading` property yet
- `youtube` videos are embedded with `iframe` and `iframe` has no `loading` property yet

Both of this cases could be worked around with JavaScript:
- non-`youtube`: set `src` from JavaScript as shown for images: [https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607](https://stackoverflow.com/questions/2321907/how-do-you-make-images-load-lazily-only-when-they-are-in-the-viewport/57389607#57389607).

  But this breaks page semantics however, we don't know how to work around that
- `youtube` videos: same as above for the `iframe`, but this should be less problematic since YouTube videos are not viewable without JavaScript anyways, and who cares about `iframe` semantics?

## ↑ Ancestors (4)

1. [Video](video.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
