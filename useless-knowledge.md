# Useless knowledge

↑ **Parent:** [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)

Install the NPM package globally and use it from the command line for a quick conversion:
```
npm install -g ourbigbook
printf 'ab\ncd\n' | ourbigbook --body-only
```
or to a file:
```
printf 'ab\ncd\n' | ourbigbook > tmp.html
```
You almost never want to do this except when [developing OurBigBook](developing-ourbigbook.md), as it won't be clear what version of `ourbigbook` the document should be compiled with. Just be a good infant and use OurBigBook [with the template](play-with-the-template.md) that contains a `package.json` via `npx`, OK?

Furthermore, the default install of Chromium on Ubuntu 21.04 uses Snap and blocks access to dotfiles. For example, in a sane NVM install, our global CSS would live under `/home/ciro/.nvm/versions/node/v14.17.0/lib/node_modules/ourbigbook/_obb/ourbigbook.css`, which gets blocked because of the `.nvm` part:
- [https://forum.snapcraft.io/t/dot-files/7062](https://forum.snapcraft.io/t/dot-files/7062)
- [https://bugs.launchpad.net/snapd/+bug/1607067](https://bugs.launchpad.net/snapd/+bug/1607067)
- [https://superuser.com/questions/1546550/chromium-81-wont-display-dotfiles-anymore](https://superuser.com/questions/1546550/chromium-81-wont-display-dotfiles-anymore)
- [https://askubuntu.com/questions/1184357/why-cant-chromium-suddenly-access-any-partition-except-for-home](https://askubuntu.com/questions/1184357/why-cant-chromium-suddenly-access-any-partition-except-for-home)
- [https://askubuntu.com/questions/1214346/as-a-user-is-there-any-way-to-change-the-confinement-of-a-snap-package](https://askubuntu.com/questions/1214346/as-a-user-is-there-any-way-to-change-the-confinement-of-a-snap-package)
One workaround is to use [`--embed-resources`](embed-resources.md), but this of course generates larger outputs.

To run master globally from source for development see: [Section "Run OurBigBook master"](run-ourbigbook-master.md). This one actually works despite the dotfile thing since your development path is normally outside of dotfiles.

Try out the JavaScript API with [lib_hello.js](lib_hello.js):
```
npm install ourbigbook
./lib_hello.js
```

## ↑ Ancestors (3)

1. [OurBigBook CLI quick start](ourbigbook-cli-quick-start.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Run OurBigBook master](run-ourbigbook-master.md)
