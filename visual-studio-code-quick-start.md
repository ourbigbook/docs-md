# Visual Studio Code quick start

↑ **Parent:** [Visual Studio Code](visual-studio-code.md)  
🏷️ **Tags:** [Quick start](quick-start.md)

First follow [play with the template](play-with-the-template.md) and ensure that you are able to run `ourbigbook` from the command line succesfully on a [project template](generate.md):
```
npx ourbigbook .
```
We would like to remove the need for this step and allow users doing everyting without the command line, but that will require some extra work: [https://github.com/ourbigbook/ourbigbook/issues/318](https://github.com/ourbigbook/ourbigbook/issues/318)

Once that is working, you can now install the extension either:
- via the VS Code UI: Ctrl + Shift + X and search for "ourbigbook", the ID is: `ourbigbook.ourbigbook-vscode`
- from the command line with:
  ```
  ext install ourbigbook.ourbigbook-vscode
  ```

We also recommend installing the "Code Spell checker" extension:
```
ext install streetsidesoftware.code-spell-checker
```
and adding the following settings to your User JSON settings file:
```
"cSpell.enableFiletypes": [
    "ourbigbook"
],
```

Next, open the downloaded folder in Visual Studio Code with:
- `Ctrl + Shift + P`
- File: Open Folder
then open a .bigb file such as index.bigb on vscode.

Now you are ready to:
- `Ctrl + Shift + B`: build all files in the folder
- `F5`: build all files in the folder, and view the HTML output for the current source file in your browser
- `Ctrl + Shift + Alt + B`: publish your project to [OurBigBook Web](ourbigbook-web.md)

Other things to try include:
- `Ctrl + T`: search for a header in any file
- type `<` to create an [internal cross file internal link](cross-file-internal-link.md) and observe autocompletion suggest header names for you

<a id="video-edit-locally-and-publish-demo-visual-studio-code"></a>
**[Video 20](#video-edit-locally-and-publish-demo-visual-studio-code). Edit locally and publish demo.** [Source](https://www.youtube.com/watch?v=Ghvlztiu6rI). This shows editing [OurBigBook Markup](ourbigbook-markup.md) and [publishing](publish-your-content.md) it using the [VS Code](visual-studio-code.md) extension.

<a id="image-screenshot-of-a-sample-ourbigbook-project-in-vs-code"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/local-editing/vscode-mathematics-calculus-derivative.png" alt="" height="800">

**[Figure 68](#image-screenshot-of-a-sample-ourbigbook-project-in-vs-code). Screenshot of a sample OurBigBook project in VS Code**.

## ↑ Ancestors (4)

1. [Visual Studio Code](visual-studio-code.md)
2. [Editor support](editor-support.md)
3. [Tooling](tooling.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Quick start](quick-start.md)
