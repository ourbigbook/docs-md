<h1 id="ourbigbook-web-next-js-unit-tests">OurBigBook Web Next.js unit tests</h1>

↑ **Parent:** [OurBigBook Web unit tests](ourbigbook-web-unit-tests.md)

By default, we don't make any requests to Next.js, because starting up Next.js is extremelly slow for regular test usage and would drive us crazy.

In regular OurBigBook Web usage through a browser, Next.js handles all GET requests for us, and the API only handles the other modifying methods like POST.

However, we are trying to keep the API working equally well for GET, and as factored out with Next.js as possible, so just testing the API GET already gives reasonable coverage.

But testing Next.js requests before deployment is a must, and is already done by default by `npm run deploy-prod` from [Heroku deployment](heroku-deployment.md), and can be done manually with:
```
npm run test-next
```
or e.g. to run just a single test:
```
npm run test-next -- -g 'api: create an article and see it on global feed'
```
for for Postgres:
```
npm run test-pg-next
```
These tests are currently very basic, and only check page status. In the future, we can
- add some HTML parsing to check for page contents as a reponse to GET, just as we already do in the [test system](test-system.md) of the [OurBigBook Library](ourbigbook-library.md)
- go all in an use a JavaScript enabled test system like Selenium to also test login and data modification from the browser

TODO: `npm run test-next` [https://github.com/ourbigbook/ourbigbook/issues/354](https://github.com/ourbigbook/ourbigbook/issues/354) is currently broken and always blows up on the second test that uses Next.js. So it works if you run one by one with `-g`, but not if you try to run all of them in one go.

If you are not making any changes to the website itself, e.g. only to the test system, then you can skip the slow rebuild with:
```
test-next-nobuild
test-pg-next-nobuild
```
Note that annoyingly, Next.js reuses the same forlder for dev and build runs, so you have to quit your dev server for this to work, otherwise the dev server just keeps writing into the folder and messing up the production build test.

Note that Next.js tests are just present inside other tests, e.g. `api: create an article and see it on global feed` also tests some stuff when not testing Next.js. Running `npm run test-next` simply enables the Next.js tests on top of the non Next.js ones that get run by default.

These tests can only be run in production mode, and so our scripts automatically rebuild every time before running the tests, which makes things quite slow. This required because in development mode, Next.js is extremelly soft, and e.g. does not raise 500 instead returning a 200 page with error messages. Bad default.

TODO:: the tests hang after running with Next.js enabled: [https://github.com/ourbigbook/ourbigbook/issues/353](https://github.com/ourbigbook/ourbigbook/issues/353)

## ↑ Ancestors (4)

1. [OurBigBook Web unit tests](ourbigbook-web-unit-tests.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
