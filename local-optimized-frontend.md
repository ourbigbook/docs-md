# Local optimized frontend

↑ **Parent:** [OurBigBook Web development](ourbigbook-web-development.md)

First run the first time setup from [local development server](local-development-server.md).

Then, when running for the first time, or whenever frontend changes are made, you need to create optimized frontend assets with:
```
npm run build-dev
```
before you finally start the server each time with:
```
npm start
```

This setup runs the Next.js server in production mode locally. Running this setup locally might help debug some front-end deployment issues.

Building like this notably runs full typescript type checking, which is a good way to find bugs early.

But otherwise you will just normally use the [local run as identical to deployment as possible](local-run-as-identical-to-deployment-as-possible.md) setup instead for development, as that makes iterations quicker are you don't have to re-run the slow `npm run build-dev` command after every frontend change.

`build-dev` is needed instead of `build` because it uses `NODE_ENV_OVERRIDE` which is needed because Next.js forces `NODE_ENV=production` and wontfixed changing it: [https://github.com/vercel/next.js/issues/4022#issuecomment-374010365](https://github.com/vercel/next.js/issues/4022#issuecomment-374010365), and that would lead to the PostgreSQL database being used, instead of the SQLite one we want.

`build` runs `npm run build-assets` on toplevel which repacks ourbigbook itself and is a bit slow. To speed things up during the development loop, you can also use:
```
npm run build-dev-nodeps
```
instead, which builds only the stuff under `web/`.

TypeScript type checking an also be run in isolation as mentioned at [Section "OurBigBook Web TypeScript type checking"](ourbigbook-web-typescript-type-checking.md) with:
```
npm run tsc
```

## ↑ Ancestors (3)

1. [OurBigBook Web development](ourbigbook-web-development.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [OurBigBook Web TypeScript type checking](ourbigbook-web-typescript-type-checking.md)
