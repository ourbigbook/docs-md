# OurBigBook Web useful queries

↑ **Parent:** [OurBigBook Web database](ourbigbook-web-database.md)

Some hacks for those that have DB access.

Change dates of all articles by a given user to a specific date:
```
select "Article"."updatedAt" from "Article" inner join "File" on "Article"."fileId" = "File".id inner join "User" on "File"."authorId" = "User"."id" and "User".username = 'barack-obama';
```

## ↑ Ancestors (5)

1. [OurBigBook Web database](ourbigbook-web-database.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
