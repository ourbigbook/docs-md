# OurBigBook Web signup IP blacklist

↑ **Parent:** [Database access-only admin](database-access-only-admin.md)

It is possible to blacklist IP and IP prefixes by adding them to the database with:
```
./heroku run web/bin/blacklist-signup-ip 123.456.789.1
```

IP prefixes can also be added to block entire ranges e.g.:
```
./heroku run web/bin/blacklist-signup-ip 123.456.789
./heroku run web/bin/blacklist-signup-ip 123.456
./heroku run web/bin/blacklist-signup-ip 123
```
would block respectively all of:
```
123.456.789.*
123.456.*
123.*
```

You can also add a note as:
```
./heroku run web/bin/blacklist-signup-ip 123.456.789.1 'IP blocked because asdf is ugly'
```

The list of blacklisted IPs can be obtained with:
```
./heroku psql -c 'SELECT * FROM "SignupBlacklistIp"'
```

## 🏷️ Tagged (1)

- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)

## ↑ Ancestors (5)

1. [Database access-only admin](database-access-only-admin.md)
2. [OurBigBook Web moderation](ourbigbook-web-moderation.md)
3. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)
