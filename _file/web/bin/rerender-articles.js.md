<h1 id="_file/web/bin/rerender-articles.js">web/bin/rerender-articles.js</h1>

↑ **Parent:** [Web CLI utils](../../../web-cli-utils.md)

Rerender all articles by all users:
```
web/bin/rerender-articles.js
```

Rerender only the articles with specified slugs:
```
web/bin/rerender-articles.js johnsmith/mathematics maryjane/physics
```

Only rerender articles by `johnsmith` and `maryjane`:
```
web/bin/rerender-articles.js -a johnsmith -a maryjane
```

Rerender articles by all authors except `johnsmith` and `maryjane`:
```
web/bin/rerender-articles.js -A johnsmith -A maryjane
```

Rerendering has to be done to see updates on OurBigBook changes that change the render output.

Notably, this would be mandatory in case of CSS changes that require corresponding HTML changes.

As the website grows, we will likely need to do a lazy version of this that marks pages as outdated, and then renders on the fly, plus a background thread that always updates outdated pages.

The functionality of this script should be called from a [migration](../../../ourbigbook-web-database-migration-setup.md) whenever such HTML changes are required. TODO link to an example. We had one at `web/migrations/20220321000000-output-update-ancestor.js` that seemed to work, but lost it. It was simple though. Just you have to instantiate your own Sequelize instance after making the model change to move any data.

## ↑ Ancestors (6)

1. [Web CLI utils](../../../web-cli-utils.md)
2. [OurBigBook Web directory structure](../../../ourbigbook-web-directory-structure.md)
3. [OurBigBook Web architecture](../../../ourbigbook-web-architecture.md)
4. [OurBigBook Web development](../../../ourbigbook-web-development.md)
5. [OurBigBook Web](../../../ourbigbook-web.md)
6. [OurBigBook Project](../../../split.md)

## ← Incoming links (3)

- [web/bin/rerender-comments.js](rerender-comments.js.md)
- [web/bin/rerender-issues.js](rerender-issues.js.md)
- [`--web-force-id-extraction`](../../../web-force-id-extraction.md)
