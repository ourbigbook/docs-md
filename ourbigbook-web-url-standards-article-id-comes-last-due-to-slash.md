# OurBigBook Web URL standards: article ID comes last due to slash

↑ **Parent:** [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)

It is a bit annoying that due to [scopes](h-scope-argument.md) being separated with `/`, we always have to put article names last in any URL (outside GET parameters) to avoid ambiguities. E.g. it would be arguably nicer to have:
```
/go/donald-trump/linear-algebra/issues
```
rather than the current:
```
/go/issues/donald-trump/linear-algebra
```
but this produces ambiguity, what if user `issues` has an article with title `Linear algebra` under scope `donald-trump`?

## ↑ Ancestors (5)

1. [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)
2. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
