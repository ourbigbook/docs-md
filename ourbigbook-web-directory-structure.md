# OurBigBook Web directory structure

↑ **Parent:** [OurBigBook Web architecture](ourbigbook-web-architecture.md)

- [web/app.js](web/app.js): server executable entry point, can also be used programmatically from Node.js
- [web/models](web/models): Sequelize database models. Most changes in this folder require the creation of a corresponding [web/migrations](web/migrations)
- [web/migrations](web/migrations): database migrations, see also: [Section "OurBigBook Web database migration setup"](ourbigbook-web-database-migration-setup.md)
- [web/pages](web/pages): Next.js URL entry points
- [web/front](web/front) and [web/front.tsx](web/front.tsx): files that can be imported from either front-end of backend. See: [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)
- [web/back](web/back) and [web/back.ts](web/back.ts): files that can be imported only from backend. See: [https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153](https://stackoverflow.com/questions/64926174/module-not-found-cant-resolve-fs-in-next-js-application/70363153#70363153)
- [web_api.js](web_api.js): helpers to access the OurBigBook HTTP REST API. These have to be outside of `web/` because [OurBigBook CLI](ourbigbook-cli.md) uses them e.g. for syncing local files to the server, and OurBigBook CLI cannot depend on OurBigBook Web components, only the other way around, otherwise we could create circular dependencies. That exact same JavaScript code is also used from the front-end! The infinite joys of homomorphic JS.

**Table of contents**

- [Web CLI utils](web-cli-utils.md)
  - [web/bin/normalize](_file/web/bin/normalize.md)
  - [web/bin/rerender-articles.js](_file/web/bin/rerender-articles.js.md)
  - [web/bin/rerender-issues.js](_file/web/bin/rerender-issues.js.md)
  - [web/bin/rerender-comments.js](_file/web/bin/rerender-comments.js.md)
  - [web/bin/set-password](_file/web/bin/set-password.md)

## ↑ Ancestors (4)

1. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
