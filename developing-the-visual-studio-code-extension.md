# Developing the Visual Studio Code extension

↑ **Parent:** [Visual Studio Code](visual-studio-code.md)  
🏷️ **Tags:** [Developing OurBigBook](developing-ourbigbook.md)

The source code for the extension is located under: [vscode](vscode)

It's the standard procedure for any extension:
- open a new workspace with just the extension at toplevel:
  - Ctrl + Shift + N
  - Ctrl + Shift + P
  - Open workspace from file
  - select [vscode/vscode.code-workspace](vscode/vscode.code-workspace)
- In the new window from any file:
  - Ctrl+Shift+P
  - Debug: Start Debugging

  This opens a new window titled "Extension Development Host". You will likely then want to open any .bigb file from that window to test out the extension
- from there on:
  - make changes on the "vscode" workspace
  - test them on the "Extension Development Host" window. To reload changes either:
    - from the Extension Host run the "Developer: Reload Window" command to make extension changes take effect. We recommend adding a shortcut "Alt + Shift + R" for that
    - from the "vscode" workspace, restart the debug proces with the "Debug: Restart" command (default shortcut "Ctrl + Shift + F5")

## ↑ Ancestors (4)

1. [Visual Studio Code](visual-studio-code.md)
2. [Editor support](editor-support.md)
3. [Tooling](tooling.md)
4. [OurBigBook Project](split.md)
