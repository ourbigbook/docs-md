# Visual Studio Code documentation

↑ **Parent:** [Visual Studio Code](visual-studio-code.md)

Supported language features:
- syntax highlighting
- auto-completion:
  - snippets: E.g. if you type in an editor window:
    ```
    \I
    ```
    it suggests the autocompletion to
    ```
    \Image[]
    ```
     and if you select it autofills with URL the clipboard text.

    Common [named arguments](named-argument.md) also have shortcuts starting with open curly brace `{`, e.g. for the [`title` argument](title-argument.md) it is `{t` (open curly brace + `t`)
    ```
    {t
    ```
    which expands to:
    ```
    {title=}
    ```
    leaving your cursor after the `=` sign.

    see their definition fn the snippts file [vscode/snippets.json](vscode/snippets.json).
  - ID autocompletion initiated by things like:
    - `<`: [internal link](internal-link.md)
    - `{tag=`: [`\H` `tag` argument](h-tag-argument.md)
    - `{parent=`: [`\H` `parent` argument](h-parent-argument.md)

    Known limitations:
    - although separate words do find good matches in this case unlike in Ctrl + T, if you auto-complete after the first word, pre existing words are duplicated, e.g.:
      - type the first word
      - space
      - start the second word
      - finish autocomplete on second word

      then the stuff before the last space remains rather than being replaced, leaving you with something like:
      ```
      <United United States>
      ```

      The bult-in markdown extension does not support this either as it uses only slash separated "IDs" in its searches.
- `Ctrl + T` "[Open symbol by name](https://code.visualstudio.com/docs/editor/editingevolved#_open-symbol-by-name)". Shows matching [Element IDs](element-id.md) such as for [headers](header.md), and allows you to quickly jump to them. It lists:
  - first lists IDs that start with the search
  - then followed by IDs that contain the search anywhere inside them

  Unfortunately, due to VS Code limitations, you cannot use spaces in the search as we would like, e.g.:
  ```
  fundamental theorem
  ```
  will not find the ID `fundamental-theorem-of-calculus`. This is because VS Code does not pass the search after the first space to the extension at all in the `provideWorkspaceSymbols` callback. It does work if you instead use the hyphen `-` ID separator as in:
  ```
  fundamental-theorem
  ```

  Using `%` SQL wildcards such as in:
  ```
  fund%ntal
  ```
  also does not work. Looking at debug logs, we see that the correct SQL queries are generated and the correct rows returned, but VS Code must be doing a hardcoded post-processing step that removes the matches afterwards, so it also seems to be out of our control.

  TODO: the built-in markdown extension handles spaces on Ctrl+T. Understand how it works.

  [ID extraction](id-extraction.md) is performed on .bigb files automatically with `ourbigbook --no-render file.bigb` whenever new changes are saved to disk e.g. with Ctrl + S. This ensures that the [ID database](cross-file-internal-link-internals.md) is kept up to date so that Ctrl + T and autocompletion will work.
- `Ctrl + Shift + O`: ID search in the current file. Somewhat of a subset of `Ctrl + T`, but works faster, is more scoped if you know your ID is in the current file, and allows you to type spaces.
- Ctrl + Click: jump to definition. If you hover over [internal cross file internal link](cross-file-internal-link.md)-like elements such anywhere over the following:
  - `<New York>`
  - `{tag=New York}`
  - `{parent=New York}`

  then the editor jumps to their definition point.
- outline, sticky scroll, breadcrumb. These features allow you to quickly navigate between headers of the current file in a tree structure. Consider adding the following shortcut to reveal the outline sidebar on `Ctrl + 3`:
  ```
  {
    "key": "ctrl+3",
    "command": "outline.focus"
  },
  ```
  As you add or remove lines to the document, the outline becomes immediately outdated. To update it, make sure to save the document (Ctrl + S) and wait a few seconds.

  Drag and drop editing gets requested from time to time but just dies to the bot:
  - [https://github.com/microsoft/vscode/issues/143192](https://github.com/microsoft/vscode/issues/143192)
  - [https://github.com/microsoft/vscode/issues/69080](https://github.com/microsoft/vscode/issues/69080)
  though in our case it wouldn't be so simple as [`\H` `parent` arguments](h-parent-argument.md) would also have to be adjusted.
- commands: all our command shortcuts are defined to only work on OurBigBook files ([`.bigb` extension](ourbigbook-markup.md)) to avoid cluttering non-OurBigBook projects. This is done as vscode does not seem to have the concept of "project type" built into it. If you want the build and launch shorcuts to work on your project for any file, also define build and launch commands under `.vscode`
  - `Build all`: save the current file is unsaved, and then build the [project toplevel directory](project-toplevel-directory.md) with `ourbigbook .`
  - `Build all and view current output file`: do `ourbigbook .` and then open the HTML output for the current file in your browser

    Known limitations: snap browsers on Ubuntu 24.04 can't access dotfiles, so CSS and JavaScript will be broken because they go under `~/.vscode` when building with the extension: [https://askubuntu.com/questions/1238211/how-to-make-snaps-access-hidden-files-and-folders-in-home#comment2676255_1238219](https://askubuntu.com/questions/1238211/how-to-make-snaps-access-hidden-files-and-folders-in-home#comment2676255_1238219) We don't know how to work around this besides not using the snap version of browsers.
  - `Publish to static website (ourbigbook.publishStatic)`: publish [static website](p-publish.md)
  - `Publish to OurBigBook Web (ourbigbook.publishWeb)`: publish to [OurBigBook Web](ourbigbook-web.md)
  - `Publish to OurBigBook Web and static (ourbigbook.publishWebAndStatic)`: publish to both [OurBigBook Web](ourbigbook-web.md) and [static website](p-publish.md)

Todo
- deployment as [static website](p-publish.md) or to [OurBigBook Web](ourbigbook-web.md) via command
- live side-by-side HTML preview, maybe we could learn a bit from the Asciidoc extension
The default markdown support is incredible and should serve as inspiration for this extension: [https://code.visualstudio.com/docs/languages/markdown](https://code.visualstudio.com/docs/languages/markdown)

Historically, [Vim](vim.md) support came first and was better developed. But that was just an ad-hoc path of least resistance, VS Code is the one we are going to actually support moving forward.

Our syntax highlighting attempts mostly to follow the official HTML style, which is perhaps the best maintained data-language. We have also had a look at the LaTeX, Markdown and Asciidoctor ones for refernce.

One current fundamental limitation of [VS Code](visual-studio-code.md) is that there is no way to preview images and mathematics inline with text: [https://stackoverflow.com/questions/52709966/vscode-is-it-possible-to-show-an-image-inside-a-text-buffer](https://stackoverflow.com/questions/52709966/vscode-is-it-possible-to-show-an-image-inside-a-text-buffer) If only it were able to do that, it would go a long way to being as good as a WYSIWYG interface.

**Table of contents**

- [Visual Studio Code options](visual-studio-code-options.md)
- [`gitAutoCommitAfterBuild`](gitautocommitafterbuild.md)

## ↑ Ancestors (4)

1. [Visual Studio Code](visual-studio-code.md)
2. [Editor support](editor-support.md)
3. [Tooling](tooling.md)
4. [OurBigBook Project](split.md)
