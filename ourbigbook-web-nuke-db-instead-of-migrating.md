# OurBigBook Web nuke DB instead of migrating

↑ **Parent:** [OurBigBook Web database migration setup](ourbigbook-web-database-migration-setup.md)

When quickly developing before we had any users, a reasonable way is to nuke the database everytime instead of spending time writing migrations. To do this, you can without creating a migration:
```
npm run deploy-prod
```
This breaks the website, because the DB is out of sync. So then you go and manually fix it up:
```
# heroku run -a ourbigbook web/bin/generate-demo-data.js --force-production --clear
```

## ↑ Ancestors (6)

1. [OurBigBook Web database migration setup](ourbigbook-web-database-migration-setup.md)
2. [OurBigBook Web database](ourbigbook-web-database.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)
