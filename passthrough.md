# Passthrough

↑ **Parent:** [Macro](macro.md)  
🏷️ **Tags:** [XSS unsafe macro](xss-unsafe-macro.md)

Dumps its contents directly into the rendered output.

This construct is not XSS safe, see: [Section "unsafeXss"](unsafexss.md).

Here for example we define a paragraph in raw HTML:
```
\Passthrough[[
<p>Hello <b>raw</b> HTML!</p>
]]
```
which renders as:



> <p>Hello <b>raw</b> HTML!</p>

And for an inline passthrough:
```
Hello \passthrough[[<b>raw</b>]] world!
```
which renders as:



> Hello \<b\>raw\</b\> world!

## ↑ Ancestors (3)

1. [Macro](macro.md)
2. [OurBigBook Markup](ourbigbook-markup.md)
3. [OurBigBook Project](split.md)
