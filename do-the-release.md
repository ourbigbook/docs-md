# Do the release

↑ **Parent:** [Release procedure](release-procedure.md)

This section describes the release procedure for [OurBigBook CLI](ourbigbook-cli.md), which is an npm package. For [OurBigBook Web](ourbigbook-web.md) deployment see: [OurBigBook Web deployment](ourbigbook-web-deployment.md).

Before the first time you release, make sure that you can login to NPM with:
```
npm login
```
This prompts you to login via the browser with 2FA. Currently you can also tick a box to not ask again for the next 5 minutes, which should be enough for the following [release](release) command. If you don't select this option, you will be prompted midway through the release command for login.

Releases should always be made with the official [https://www.npmjs.com/~ourbigbook-admin](https://www.npmjs.com/~ourbigbook-admin) NPM user.

Then, every new release can be done automatically with the [release](release) script, e.g. to release a version 0.7.2:
```
./release 0.7.2
```
or to just increment the minor version, e.g. from the current `0.7.1` to `0.7.2` you could can omit the version argument:
```
./release
```
That script does the following actions, aborting immediately if any of them fails:
- runs [the tests](test-system.md)
- publishes this documentation
- updates `version` in `package.json`
- creates a release commit and a git tag for it
- pushes the source code
- publishes the NPM package

## ↑ Ancestors (3)

1. [Release procedure](release-procedure.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Visual Studio Code extension release procedure](visual-studio-code-extension-release-procedure.md)
