# OurBigBook Web database normalization

↑ **Parent:** [OurBigBook Web database](ourbigbook-web-database.md)

We currently have some intentional denormalization in our database e.g.:
- counts such as: user reputation, article issue and follower counts, issue comment and follower counts
- [nested sets](nested-set.md)

These dernormalizations are not ideal, but they make things a bit easier, and some of them are almost certainly faster.

To keep things slightly saner, the [web/bin/normalize](_file/web/bin/normalize.md) script can be used to view, check and update dernormalized data.

## ↑ Ancestors (5)

1. [OurBigBook Web database](ourbigbook-web-database.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
