# OurBigBook Web admin

↑ **Parent:** [OurBigBook Web moderation](ourbigbook-web-moderation.md)

Each user has an `admin` property which when set to `true` allows the user to basically view and change anything for themselves and other users. E.g. admins can see private data of any user such as emails, or modify users usernames.

Some actions are not possible currently because they were originally hardcoded for "do action for the current user" rather than "do action for target user", but all of those are intended to be converted. E.g. that is currently the case for like/unlike, follow/unfollow from the API.

In order to mark a user as admin, direct DB acceess is required.

For example, to make user `barack-obama` admin on a development run the [web/bin/make-admin](web/bin/make-admin) script:
```
web/bin/make-admin barack-obama
```
Admin priviledges can be revoked with the `-f` (`--false`) flag:
```
web/bin/make-admin -f barack-obama
```

The same command works in a [Heroku deployment](heroku-deployment.md) where you can run:
```
heroku run -a ourbigbook web/bin/make-admin -f barack-obama
```

**Table of contents**

- [Account locking](account-locking.md)

## ↑ Ancestors (4)

1. [OurBigBook Web moderation](ourbigbook-web-moderation.md)
2. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Automatic topic linking](automatic-topic-linking.md)
- [Can my OurBigBook.com content be edited or removed by other users?](can-my-ourbigbook-com-content-be-edited-or-removed-by-other-users.md)
- [Database access-only admin](database-access-only-admin.md)
