# Staging deployment

↑ **Parent:** [Heroku deployment](heroku-deployment.md)

Before pushing any new changes, and especially ones that seem dangerous, it is a good idea to first deploy to a staging server.

We have a staging server running at: [https://ourbigbook-staging.herokuapp.com/](https://ourbigbook-staging.herokuapp.com/)

To set it up, we just follow the exact same steps as for [Heroku deployment](heroku-deployment.md) but with a different app ID. E.g. using the `ourbigbook-staging` heroku project ID:
```
git remote add staging https://git.heroku.com/ourbigbook-staging.git
heroku addons:create -a ourbigbook-staging --confirm ourbigbook-staging heroku-postgresql:hobby-dev
heroku config:set -a ourbigbook-staging SECRET="$(tr -dc A-Za-z0-9 </dev/urandom | head -c 256)"
npm run deploy-staging
```

To copy the main database in staging we can follow the instructions at: [https://stackoverflow.com/questions/10673630/how-do-i-transfer-production-database-to-staging-on-heroku-using-pgbackups-gett](https://stackoverflow.com/questions/10673630/how-do-i-transfer-production-database-to-staging-on-heroku-using-pgbackups-gett) Considering a production Heroku app ID of `ourbigbook`:
```
heroku maintenance:on -a ourbigbook-staging &&
heroku pg:copy ourbigbook::DATABASE_URL DATABASE_URL -a ourbigbook-staging &&
heroku maintenance:off -a ourbigbook-staging
```

To get a shell on the stating server you can run:
```
heroku run -a ourbigbook-staging bash
```

## ↑ Ancestors (5)

1. [Heroku deployment](heroku-deployment.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
