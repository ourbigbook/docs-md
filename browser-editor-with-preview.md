# Browser editor with preview

↑ **Parent:** [Editor support](editor-support.md)

There are two versions of this editor:
- [static editor](static-editor.md): a browser-only toy/demo with no persistent storage
- [web editor](web-editor.md): this is editor present in [OurBigBook Web](ourbigbook-web.md). It is linked to the database, and has further features added on top of the [static editor](static-editor.md).

Issues for the editor are being tracked under: [https://github.com/ourbigbook/ourbigbook/labels/web-editor](https://github.com/ourbigbook/ourbigbook/labels/web-editor)

We must achieve an editor setup with synchronized live side-by-side preview.

Likely, we will first do a non WYSIWYG editor with side by side preview with scroll sync.

Then, if the project picks up steam, we can start considering a full WYSIWYG.

It would be amazing to have a WebKit interface that works both on browser for the and locally.

Possibilities we could reuse:
- CKeditor [https://ckeditor.com/](https://ckeditor.com/) Used e.g. by Trilium Notes.
- Editor.js

  Returns JSON AST!


  - website: [https://editorjs.io/](https://editorjs.io/)
  - source: [https://github.com/codex-team/editor.js](https://github.com/codex-team/editor.js)
  - WYSIWYG: yes
  - preview scroll sync: yes
- StackEdit
  - markup implementation: PageDown
  - website: [https://stackedit.io](https://stackedit.io)
  - source: [https://github.com/benweet/stackedit](https://github.com/benweet/stackedit)
  - demo: [https://stackedit.io/app](https://stackedit.io/app)
  - WYSIWYG: no
  - preview scroll sync: yes
- Editor.md
  - website: [https://github.com/pandao/editor.md](https://github.com/pandao/editor.md)
  - source: [https://github.com/pandao/editor.md](https://github.com/pandao/editor.md)
  - demo: [https://pandao.github.io/editor.md](https://pandao.github.io/editor.md)
  - WYSIWYG: no
  - preview scroll sync: yes but buggy when tested 2019-12-12 on live website
- [markdown-it](https://github.com/markdown-it/markdown-it)

  Custom editor and highlight via [highlight.js](https://github.com/highlightjs/highlight.js/).


  - markup implementation: custom
  - website: [https://markdown-it.github.io](https://markdown-it.github.io)
  - source: [https://github.com/markdown-it/markdown-it](https://github.com/markdown-it/markdown-it)
  - WYSIWYG: no
  - preview scroll sync: yes
  - editor hangs on large input: yes
- Quill.md
  - website: [https://quilljs.com](https://quilljs.com)
  - source: [https://github.com/quilljs/quill/](https://github.com/quilljs/quill/)
  - demo: [https://pandao.github.io/editor.md](https://pandao.github.io/editor.md)
  - WYSIWYG: yes
  - markdown output: no [https://github.com/quilljs/quill/issues/74](https://github.com/quilljs/quill/issues/74)
- [https://ui.toast.com/tui-editor/](https://ui.toast.com/tui-editor/)
- [https://www.froala.com/wysiwyg-editor](https://www.froala.com/wysiwyg-editor)

**Table of contents**

- [Static editor](static-editor.md)
- [Web editor](web-editor.md)

## ↑ Ancestors (3)

1. [Editor support](editor-support.md)
2. [Tooling](tooling.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (6)

- [Conversion process overview](conversion-process-overview.md)
- [`Dist` directory](dist-directory.md)
- [`\H` `parent` argument](h-parent-argument.md)
- [`--log headers`](log-headers.md)
- [Static editor](static-editor.md)
- [Vim](vim.md)
