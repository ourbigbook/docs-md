# Making concurrent changes to ourbigbook and the extension

↑ **Parent:** [Visual Studio Code](visual-studio-code.md)

Sometimes you need to change ourbigbook files like [index.js](index.js) when working on a new extension feature.

TODO: we don't have a neat way to handle this now. Currently;  
[vscode/package.json](vscode/package.json)  
uses fixed `ourbigbook` versions such as:
```
  "dependencies": {
    "ourbigbook": "0.9.11"
```
and therefore does not pick up changes made to [index.js](index.js).

To work around that, you can hack that line to:
```
  "dependencies": {
    "ourbigbook": ".."
```
and:
```
cd vscode
npm install
```

The reason we don't use the `..` by default is that we are unable to release the extension with the `..` for an unknown reason because then:
```
npx vsce package
```
is failing with:
```
Executing prepublish script 'npm run vscode:prepublish'...

> ourbigbook-vscode@0.0.26 vscode:prepublish
> npm run compile


> ourbigbook-vscode@0.0.26 compile
> tsc -p ./

 ERROR  Command failed: npm list --production --parseable --depth=99999 --loglevel=error
npm ERR! code ELSPROBLEMS
npm ERR! invalid: katex@v0.11.1 /home/ciro/bak/git/ourbigbook/node_modules/katex

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/ciro/.npm/_logs/2024-08-05T15_51_22_124Z-debug-0.log
```
One thing we could do is to play it really nasty and hack `..` to a fixed version for relese, then hack it back to `..` immediately, always requiring a ourbigbook release for each vscode release.

If you use the `..` hack, besides undoing the `..` change, before releasing you have to:
```
cd vscode
rm -rf node_modules package-lock.json
```
otherwise the error does not go away.

## ↑ Ancestors (4)

1. [Visual Studio Code](visual-studio-code.md)
2. [Editor support](editor-support.md)
3. [Tooling](tooling.md)
4. [OurBigBook Project](split.md)
