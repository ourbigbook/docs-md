# OurBigBook Web analytics

↑ **Parent:** [Database access-only admin](database-access-only-admin.md)

[OurBigBook Web](ourbigbook-web.md) supports the following types of analytics:
- Google Analytics. TODO: the Google Analytics ID is currently hardcoded under [web/front/config.js](web/front/config.js) `googleAnalyticsId: 'G-R721ZZTW7L'`, we should instead take it from an environment variable
- our simple built-in analytics to better view referrers. At some point Google Analytics stopped showing clear referrer paths, and so we started storing out own real quick. There is currently no UI for it, you just have to query the database e.g. with:
  ```
  printf '\\a\nSELECT referrer,path,ip,"createdAt" FROM "Request" ORDER BY "createdAt" DESC LIMIT 1000' | ./heroku psql DATABASE_URL
  ```
  You can also blacklist domains to reduce referrer spam with [web/bin/blacklist-referrer-domain](web/bin/blacklist-referrer-domain):
  ```
  ./heroku web/bin/blacklist-referrer-domain binance.com
  ```
  You can list the blacklisted domains with:
  ```
  ./heroku psql -c 'SELECT domain FROM "ReferrerDomainBlacklist" ORDER BY domain ASC'
  ```
  Here's a small open database that might help: [https://github.com/matomo-org/referrer-spam-list](https://github.com/matomo-org/referrer-spam-list).

  Local testing can be done on [PostgreSQL](ourbigbook-web-postgresql.md) with the help of:
  ```
  curl -H 'Referrer:http://exmaple.com' http://localhost:3000/qwer &>/dev/null && web/bin/psql 'select * from "Request"'
  ```

  We later learned that this feature is completely useless because [browsers are actually not sending paths anymore](https://stackoverflow.com/questions/6762258/when-browser-sets-the-referrer-in-http-request-header/79469565#79469565). But it's fun.

## ↑ Ancestors (5)

1. [Database access-only admin](database-access-only-admin.md)
2. [OurBigBook Web moderation](ourbigbook-web-moderation.md)
3. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
