# Heroku deployment

↑ **Parent:** [OurBigBook Web deployment](ourbigbook-web-deployment.md)

Got it running perfectly at as of April 2021 [https://ourbigbook.com](https://ourbigbook.com) with the following steps.

Initial setup for a Heroku project called `ourbigbook`:
```
sudo snap install --classic heroku
heroku login
./heroku git:remote
git remote rename heroku prod
# Automatically sets DATABASE_URL.
./heroku addons:create heroku-postgresql:hobby-dev
# We need this to be able to require("ourbigbook")
./heroku config:set SECRET="$(tr -dc A-Za-z0-9 </dev/urandom | head -c 256)"
# Password of users generated with ./web/bin/generate-demo-data
./heroku config:set OURBIGBOOK_DEMO_USER_PASSWORD="$(tr -dc A-Za-z0-9 </dev/urandom | head -c 20)"
# You can get it later to login with the demo users from the Heroku web interface
```
To finish things off, you must now:
- setup [OurBigBook Web email sending](ourbigbook-web-email-sending.md), e.g. with [OurBigBook Web email sending with Sendgrid](ourbigbook-web-email-sending-with-sendgrid.md). We haven't found a free method integrated with Heroku currently, so using this separate Sendgrid setup initially.
- optional but highly recommended: setup reCAPTCHA: [Section "OurBigBook Web reCAPTCHA setup"](ourbigbook-web-recaptcha-setup.md)
- optional: setup [Section "OurBigBook VPN blocking"](ourbigbook-vpn-blocking.md)

Additionally, you also need to setup the PostgreSQL test database for both OurBigBook CLI and OurBigBook Web as documented at [Section "OurBigBook Web PostgreSQL setup"](ourbigbook-web-postgresql-setup.md):
```
web/bin/pg-setup ourbigbook-cli
```

Then deploy with:
```
cd web
npm run deploy-prod
```

Get an interactive shell on the production server:
```
./heroku run bash
```
From there you could then for example update the [demo data](demo-data.md) with:
```
cd web
bin/generate-demo-data.js --force-production
```
This should in theory not affect any real user data, only the demo articles and users, so it might be safe. In theory!

Alternatively, we could do this at once with;
```
./heroku run web/bin/generate-demo-data.js --force-production
```

Drop into a PostgreSQL shell on production:
```
./heroku psql
```
Of course, any writes could mean loss of user data!

Run a query directly from your terminal:
```
./heroku psql -c 'SELECT username,email FROM "User" ORDER BY "createdAt" DESC LIMIT 50'
```

If some spurious bugs crashes the server, you might want to restart it with:
```
./heroku restart
```

**Table of contents**

- [heroku](_file/heroku.md)
- [Upgrade PostgreSQL database](upgrade-postgresql-database.md)
- [Custom domain name setup](custom-domain-name-setup.md)
- [Staging deployment](staging-deployment.md)
- [Heroku debugging](heroku-debugging.md)
  - [Download Heroku database and restore it locally](download-heroku-database-and-restore-it-locally.md)
- [Dependency organization](dependency-organization.md)

## ↑ Ancestors (4)

1. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (5)

- [OurBigBook Web admin](ourbigbook-web-admin.md)
- [OurBigBook Web Next.js unit tests](ourbigbook-web-next-js-unit-tests.md)
- [OurBigBook Web performance log](ourbigbook-web-performance-log.md)
- [OurBigBook Web reCAPTCHA setup](ourbigbook-web-recaptcha-setup.md)
- [Staging deployment](staging-deployment.md)
