# OurBigBook Web API standards

↑ **Parent:** [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)

In the API article slugs are always passed as a GET parameter, unlike in the case of browser visible URLs. This is because we don't care about having:
- nice human readable URLs
- ISR, at least for now
so the `id=` parameter is always used.

For now there is no API that returns single items: getting a single item is done simply using a filter that uniquely selects a single element, e.g.:
```
/api/articles?id=johnsmith/mathematics
```
Maybe this will change if someday we ever de to have full vs minimized versions of API objects. But then at that point we might as well go to GraphQL.

## ↑ Ancestors (5)

1. [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)
2. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)
