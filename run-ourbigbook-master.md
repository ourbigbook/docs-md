# Run OurBigBook master

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

Install master globally on your machine:
```
git clone --recursive https://github.com/ourbigbook/ourbigbook
cd ourbigbook
npm link
npm link ourbigbook
npm run build-assets
```
so you can now run the `ourbigbook` command from any directory in your computer, for example to convert the ourbigbook documentation itself:
```
ourbigbook .
```
Note that this repository uses [`outputOutOfTree`](ourbigbook-json/outputoutoftree.md), and so the output will be present at `_out/html/index.html` rather than `index.html`.

We also have a shortcut for `npm link` and `npm link ourbigbook`:
```
npm run link
```

`npm run link` produces symlinks so that any changes made to the Git source tree will automatically be visible globally, see also: [https://stackoverflow.com/questions/28440893/install-a-locally-developed-npm-package-globally](https://stackoverflow.com/questions/28440893/install-a-locally-developed-npm-package-globally) The symlink structure looks like:
```
/home/ciro/ourbigbook/node_modules/ourbigbook -> /home/ciro/.nvm/versions/node/v14.17.0/lib/node_modules/ourbigbook -> /home/ciro/ourbigbook
```

As mentioned at [useless knowledge](useless-knowledge.md), most users don't want global installations of OurBigBook. But this can be handy during development, as you can immediately see how your changes to OurBigBook source code affect your complex example of interest. For example, Ciro developed a lot of OurBigBook by hacking [https://github.com/cirosantilli/cirosantilli.github.io](https://github.com/cirosantilli/cirosantilli.github.io) directly with OurBigBook `master`.

Just remember that if you add a new dependency, you must redo the symlinking business:
```
npm install <dependency>
npm run link
```
Asked if there is a better way at: [https://stackoverflow.com/questions/59389027/how-to-interactively-test-the-executable-of-an-npm-node-js-package-during-develo](https://stackoverflow.com/questions/59389027/how-to-interactively-test-the-executable-of-an-npm-node-js-package-during-develo). The symlink business can be undone with:
```
npm unlink
rm node_modules/ourbigbook
```

**Table of contents**

- [Run an isolated OurBigBook master](run-an-isolated-ourbigbook-master.md)

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Run an isolated OurBigBook master](run-an-isolated-ourbigbook-master.md)
- [Useless knowledge](useless-knowledge.md)
