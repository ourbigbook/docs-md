# OurBigBook Web UI guidelines

↑ **Parent:** [OurBigBook Web architecture](ourbigbook-web-architecture.md)

- nav tabs
  - are icon-separated, e.g.: "(home icon) Home (article icon) Top Articles (article icon) Latest articles'
  - every title-like (e.g. pages, table headers) thing and links to title-like things are "Sentence cased", i.e.:
    - the first letter uppercase
    - others are lowercase or uppercase if proper nouns
- things that users can click to "take actions" (usually modify the database) show as buttons. Things that users can click to view things show as links. Exmaples of actions:
  - like, subscribe
  - create article/issue/comment
  - go to a separate new/edit article/issue page. This is strictly technically speaking just a link, but it is closely related to creating something new, so it feels more intuitive for it to be a button
- when logged off:
  - stateful actions like "create article" or "like article" show as if logged in, but redirected to signup page. Unless it is possible for user to create significant content and then lose it, e.g. type in a new comment body and only notice later that he cannot submit.

**Table of contents**

- [OurBigBook Web with JavaScript disabled](ourbigbook-web-with-javascript-disabled.md)

## ↑ Ancestors (4)

1. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
