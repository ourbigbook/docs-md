# Vim

↑ **Parent:** [Editor support](editor-support.md)

You can install the support with [Vundle](https://github.com/VundleVim/Vundle.vim) with:
```
set nocompatible
filetype off
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
Plugin 'gmarik/vundle'
let g:snipMate = {}
let g:snipMate.snippet_version = 1
Plugin 'MarcWeber/vim-addon-mw-utils'
Plugin 'tomtom/tlib_vim'
Plugin 'garbas/vim-snipmate'
Plugin 'ourbigbook/ourbigbook', {'rtp': 'vim'}
```
or by directly dropping the files named below under your `~/.vim/`, e.g. `vim/syntax/ourbigbook.vim`

The following support is provided:
- [vim/syntax/ourbigbook.vim](vim/syntax/ourbigbook.vim): syntax highlighting.

  As for other programming languages, this cannot be perfect without actually parsing, which would be slow for larger files.

  But even the imperfect approximation already covers a lot of the most cases.

  Notably it turns off spelling from parts of the document like URLs and code which would otherwise contain many false positive spelling errors.
- [vim/snippets/ourbigbook.snippets](vim/snippets/ourbigbook.snippets): snippets for [https://github.com/honza/vim-snippets](https://github.com/honza/vim-snippets), which you also have to install first for them to work.

  For example, with those snippets installed, you can easily create links to headers. Suppose you have:
  ```
  = My long header
  ```
  To create an [internal link](internal-link.md) to it you can:
  - copy `My long header` to the clipboard, see copy to clipboard shortcuts at: [https://stackoverflow.com/questions/3961859/how-to-copy-to-clipboard-in-vim/67890119#67890119](https://stackoverflow.com/questions/3961859/how-to-copy-to-clipboard-in-vim/67890119#67890119)
  - type `\x` and then hit tab
  and it will automatically expand to:
  ```
  \x[my-long-header]
  ```
  This provides a reasonable alternative for ID calculation, until a ctags-like setup gets implemented (never/[browser editor with preview](browser-editor-with-preview.md)-only? ;-))

  Similarly for [`\H` `parent` argument](h-parent-argument.md) you can do:
  ```
  {p
  ```
  would expand to:
  ```
  {parent=my-long-header}
  ```

  Syntax highlighting can likely never be perfect without a full parser (which is slow), but even the imperfect approximate setup (as provided for most other languages) is already a huge usability improvement.

  We will attempt to err on the side of "misses some stuff but does not destroy the entire page below" whenever possible.
- mappings:
  - `<leader>f`, which usually means `,f` (comma then F): start searching for a header in the current file. Does a regular `/` search without opening any windows, to is it very ligthweight. Mnemonic: "Find".
  - `<leader>h` (requires [Fugitive](https://github.com/tpope/vim-fugitive) to be installed): sets up the `ObbGitGrep` command, which  searches for header across all git tracked files in the current Git repository. After `,g` you are left in the prompt with:
    ```
    ObbGitGrep
    ```
    so if you complete that by:
    ```
    ObbGitGrep animal kingdom
    ```
    it will match headers that start with `animal kingdoom` case insentively, e.g.:
    ```
    = Animal kingdom tree
    = Animal kingdom book
    ```
    Vim regular expressions are accepted, e.g. if you don't want it to start with the search pattern:
    ```
    ObbGitGrep .*animal kingdom
    ```
    The command opens a new tab (technically a "Vim error window") containing all matches, where you can click Enter to open one of them.

    Mnemonic: "Header search".

A simple way to develop is to edit the Vundle repository directly under `~/.vim/bundle/ourbigbook`.

## ↑ Ancestors (3)

1. [Editor support](editor-support.md)
2. [Tooling](tooling.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Visual Studio Code documentation](visual-studio-code-documentation.md)
