# Visual Studio Code extension release procedure

↑ **Parent:** [Release procedure](release-procedure.md)

The [VS Code extension](visual-studio-code.md) is automatically updated and released by the standard release procedure: [Section "Do the release"](do-the-release.md).

This is done so that the extension always includes the latest version of the ourbigbook package.

This is not ideal as we would like for the extension to use the ourbigbook package version specified on each project's package.json.

However that is not easy to achieve, because in some cases we need to refactor ourbigbook to allow for a new extension feature, creating incompatibilities.

So for now, we ignore the problem and take the "easy to get started" approach of "always ship ourbigbook with the extension".

If changes are made only to the extension, it is also possible to release a new version of the extension alone with [release-vscode](release-vscode):

```
./relese-vscode
```

## ↑ Ancestors (3)

1. [Release procedure](release-procedure.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
