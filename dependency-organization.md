# Dependency organization

↑ **Parent:** [Heroku deployment](heroku-deployment.md)

On the toplevel we have:
- `.`: OurBigBook package
- `web/`: [OurBigBook Web](ourbigbook-web.md) package that depends on the local OurBigBook package through relative path `..`

  Every require outside of `web/` must be relative, except for executables such as [ourbigbook](ourbigbook) or demos such as [lib_hello.js](lib_hello.js), or else the deployment will break.

  This is because we don't know of a super clean way of adding the toplevel `ourbigbook` package to the search path as `npm run link` does not work well on Heroku.

  A known workaround to allow `npm run build-assets` is done at: [web/build.sh](web/build.sh).

Currently, Heroku deployment does the following:
- install both `dependencies` and `devDependencies`
- `npm run build`
- remove `devDependencies` from the final output to save space and speed some things up

  The `devDependencies` should therefore only contain things which are needed for the build, typically asset compressors like Webpack, but not components that are required at runtime.

This setup creates some conflict between what we want for OurBigBook command line users, and Heroku deployment.

Notably, OurBigBook command line users will want SQLite, and Heroku never, and SQLite installation is quite slow.

Since we were unable to find any way to make things more flexible on the `package.json` with some kind of optional depenency, for now we are just hacking out any dependencies that we don't want Heroku to install at all from [package.json](package.json) and [web/package.json](web/package.json) with `sed` rom [heroku-prebuild](heroku-prebuild).

Further discussion at: [https://github.com/ourbigbook/ourbigbook/issues/156](https://github.com/ourbigbook/ourbigbook/issues/156)

## ↑ Ancestors (5)

1. [Heroku deployment](heroku-deployment.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
