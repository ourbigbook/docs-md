# OurBigBook Web URL standards

↑ **Parent:** [OurBigBook Web architecture](ourbigbook-web-architecture.md)

This section describes rules for normally browser-visible URLs of the website. These rules do not apply to the Web API, see [OurBigBook Web API standards](ourbigbook-web-api-standards.md) for Web API URL standards.

It should be impossible to have upper case characters on any URL of the website. Words should be separated by hyphens `-` instead.

Use the usual gramatical ordering for action object pairs, e.g.:
- `new-discussion`
- `edit-discussion`
instead of:
- `discussion-new`
- `discussion-edit`
The latter is tempting to group all "Discussion" actions under a prefix, but let's use the nice grammar instead.

GET parameters should always be alphabetically ordered by key, e.g.:
```
?ab=1&cd=2
```
rather than:
```
?cd=2&ab=1
```

**Table of contents**

- [OurBigBook Web URL standards: GET param vs url component](ourbigbook-web-url-standards-get-param-vs-url-component.md)
- [OurBigBook Web URL standards: article ID comes last due to slash](ourbigbook-web-url-standards-article-id-comes-last-due-to-slash.md)
- [OurBigBook Web API standards](ourbigbook-web-api-standards.md)

## ↑ Ancestors (4)

1. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
