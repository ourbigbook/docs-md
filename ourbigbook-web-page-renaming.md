# OurBigBook Web page renaming

↑ **Parent:** [OurBigBook Web user manual](ourbigbook-web-user-manual.md)

The current setup works as follows.

Suppose you have a page titled:
```
Calculus
```
and therefore with an ID `calculus` that appears under: [https://ourbigbook.com/barack-obama/calculus](https://ourbigbook.com/barack-obama/calculus)

Suppose you want to rename it to "Calculus 2" to have an ID of `calculus-2`.

The procedure is:
- set title to `Caculus 2`
- set `Calculus` as a [synonym](h-synonym-argument.md) of the article, but adding to the top of the article body:

  ```
  Calculus
  {synonym}
  ```

As a result of this:
- the page will now be hosted under [https://ourbigbook.com/barack-obama/calculus](https://ourbigbook.com/barack-obama/calculus)
- [https://ourbigbook.com/barack-obama/calculus-2](https://ourbigbook.com/barack-obama/calculus-2) becomes a redirect to [https://ourbigbook.com/barack-obama/calculus](https://ourbigbook.com/barack-obama/calculus)
- articles that point with an [internal link](internal-link.md) to `calculus` are unmodified, and still link to: [https://ourbigbook.com/barack-obama/calculus](https://ourbigbook.com/barack-obama/calculus). But that link works due to the redirect.

This is not super user friendly, and could be made better by:
- moving `synonym` from source to widgets: [move all header metadata from source to HTML in Widgets](todo/web-header-metadata-to-widgets.md)
- actually update all references on other files to the new value. This could be done e.g. by creating a worker thread, and mark all references as outdated.

## ↑ Ancestors (3)

1. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Local header deletion on web upload](local-header-deletion-on-web-upload.md)
