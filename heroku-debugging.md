# Heroku debugging

↑ **Parent:** [Heroku deployment](heroku-deployment.md)

To [log database queries](log-database-queries.md) you can run:
```
./heroku config:set DEBUG='*:sql:*'
```

You then then see them with other logs at:
```
./heroku logs -t
```

Disable these verbose logs once you're done:
```
./heroku config:unset DEBUG
```

**Table of contents**

- [Download Heroku database and restore it locally](download-heroku-database-and-restore-it-locally.md)

## ↑ Ancestors (5)

1. [Heroku deployment](heroku-deployment.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
