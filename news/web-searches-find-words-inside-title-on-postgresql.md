# Web searches find words inside title on PostgreSQL

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [OurBigBook Web PostgreSQL](../ourbigbook-web-postgresql.md), [`-W`, `--web`](../web.md)

When searching articles and topics on [OurBigBook Web PostgreSQL](../ourbigbook-web-postgresql.md), which is the case for [OurBigBook.com](../ourbigbook-com.md):
- each searched word can match exactly within any word of article [IDs](../element-id.md)
- the last word is considered as a prefix, and matches the start of any word of the ID
Previously, searches would only work if they were exactly a prefix of the title ID.

For example, if you search:
```
calculus fun
```
then it will match titles such as:
```
Fundamental theorem of calculus
```
since it contains both:
- the full word `calculus`
- `fundamental` which contains the prefix `fun`

This feature implemented efficiently by using PostgreSQL's built-in full text search module.

<a id="image-ourbigbook-web-search-highlighting-full-text-search"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/search/full-text-calculus-fun-arrow.png" alt="" height="738">

**[Figure 8](#image-ourbigbook-web-search-highlighting-full-text-search). OurBigBook Web search highlighting full text search**. [Source](https://ourbigbook.com/go/articles?body=false&search=calculus%20fun).

Announcements:
- [https://mastodon.social/@ourbigbook/114009281220745242](https://mastodon.social/@ourbigbook/114009281220745242)
- [https://x.com/OurBigBook/status/1890828492222124218](https://x.com/OurBigBook/status/1890828492222124218)
- [https://www.linkedin.com/feed/update/urn:li:share:7296594330725568512](https://www.linkedin.com/feed/update/urn:li:share:7296594330725568512)
- [https://www.facebook.com/OurBigBook/posts/pfbid02oxfZ1kpfvPexovaEKqcE7D2MSEgQFM25ZdsQDXCLpV9C6uREKGNGV2A4E9MGuWi8l](https://www.facebook.com/OurBigBook/posts/pfbid02oxfZ1kpfvPexovaEKqcE7D2MSEgQFM25ZdsQDXCLpV9C6uREKGNGV2A4E9MGuWi8l)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)

## ← Incoming links (1)

- [OurBigBook Web search](../ourbigbook-web-search.md)
