# OurBigBook Web URL standards: scoped routes

↑ **Parent:** [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)

Browser URLs use `/-/` to separate a user or article [ID](element-id.md) from page actions:
- global pages: `/-/users`, `/-/articles`, `/-/files`
- user pages: `/username/-/articles`, `/username/-/files`, `/username/-/settings`
- article pages: `/username/my/article/-/discussions`, `/username/my/article/-/edit`
- individual [discussions](ourbigbook-web-discussions.md): `/username/my/article/-/discussion/1`

For the user's home article, discussions and comments use `/username/-/home/discussions` and `/username/-/home/comments`. This distinguishes them from `/username/-/discussions` and `/username/-/comments`, which list content authored by that user. The previous `/username/-/article/discussions` and `/username/-/article/comments` URLs permanently redirect to these home article URLs.

The `-` path component is a [reserved ID](reserved-id.md) in both article IDs and uploaded file paths, to prevent ambiguity. `go` remains a reserved username. Old `/go/` URLs permanently redirect to their new locations, preserving query parameters. Ordinary article URLs and [`/api` routes](ourbigbook-web-api-standards.md) keep their existing forms.

File URLs use the same namespace on [static websites](p-publish.md) and [OurBigBook Web](ourbigbook-web.md):
- `/-/file/path`: [file preview page](file-output-directory.md); on web, `/username/-/file/path`
- `/-/raw/path`: [original file bytes](raw-directory.md); on web, `/username/-/raw/path`
- `/-/dir/path`: [directory listing](dir-directory.md); on web, `/username/-/dir/path`
Static runtime assets and the [standalone editor](browser-editor-with-preview.md) use the [`/-/obb/` directory](obb-directory.md). Static file preview pages retain their usual `.html` extension when enabled. Temporary element anchors use `#-/1`, `#-/2` and so on. Named page anchors use the same namespace: `#-/toc`, `#-/ancestors`, `#-/incoming-links`, `#-/synonyms`, `#-/tagged`, `#-/comments`, `#-/comment-1`, and `#-/metadata`.

The web migration `21000101000041-reserved-path-namespace.js` updates stored file article IDs, references, cached AST paths and local profile image URLs. It preserves uploaded bytes, storage paths, source text and rendered HTML. It runs through the normal [deployment migration setup](ourbigbook-web-database-migration-setup.md); locally, run `cd web && ./bin/sync-db.js`. Legacy web `/_file/`, `/_raw/` and `/_dir/` URLs redirect permanently to the new paths.

After migrating, rerender articles, discussions and comments to regenerate their links and anchors from source:
```
web/bin/rerender-articles.js
web/bin/rerender-issues.js
web/bin/rerender-comments.js
```
See [web/bin/rerender-articles.js](-/file/web/bin/rerender-articles.js.md) for rerender options. Named anchors and comment scopes need no database transformation; `21000101000042-named-anchor-namespace.js` is retained as a no-op for migration history compatibility.

Regenerate static websites with the updated [OurBigBook CLI](ourbigbook-cli.md) and [`--force-render`](force-render.md) to publish the new paths and temporary anchors. If you keep `.bigb` sources under `_file/`, move that source directory to the [`-/file/` directory](file-input-directory.md) before rebuilding. The CLI invalidates cached legacy file IDs automatically, and existing [`\x[_file/path]` source references](internal-link.md) still resolve. Old static URLs require redirects configured on the host if they must remain available.

## ↑ Ancestors (5)

1. [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)
2. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
