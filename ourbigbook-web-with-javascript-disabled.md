# OurBigBook Web with JavaScript disabled

↑ **Parent:** [OurBigBook Web UI guidelines](ourbigbook-web-ui-guidelines.md)

It is intended that OurBigBook Web be readable with JavaScript disabled. This has the following advantages:
- reduces flickering on page load for users that JavaScript enabled
- may help with SEO
- helps with Web archiving. The Wayback Machine for example is notably bad with JavaScrip
- helps privacy freaks who have their JavaScript turned off

Pages should look exactly the same with JavaScript turned on or off.

Page interactive behaviour may differ slighly. Notably, due to [OurBigBook Web dynamic article tree](ourbigbook-web-dynamic-article-tree.md), clicking links with JavaScript off always opens a new page `/username/myid` rather than going to `#myid` if the target [Element ID](element-id.md) is already visible in the current page.

User input and even login is not intended to be necessarily possible however, and will likely be always broken.

## ↑ Ancestors (5)

1. [OurBigBook Web UI guidelines](ourbigbook-web-ui-guidelines.md)
2. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Features](features.md)
