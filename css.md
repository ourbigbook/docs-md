# CSS

↑ **Parent:** [Developing OurBigBook](developing-ourbigbook.md)

Our CSS is located at [main.scss](main.scss) and gets processed through [Sass](https://sass-lang.com).

To generate the CSS during development after any changes to that file, you must run:
```
npm run sass
```
which generates the final CSS file:
```
main.css
```

You then need to explicitly include that `main.css` file in your [`--template`](template.md). For example, our [ourbigbook.liquid.html](ourbigbook.liquid.html) contains a line:
```
<link rel="stylesheet" type="text/css" href="{{ root_relpath }}main.css">
```
where `root_relpath` is explained under [Section "`--template`"](template.md).

**Table of contents**

- [`ourbigbook.common.scss`](ourbigbook-common-scss.md)
- [Mobile guidelines](mobile-guidelines.md)

## ↑ Ancestors (2)

1. [Developing OurBigBook](developing-ourbigbook.md)
2. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Overview of files in this repository](overview-of-files-in-this-repository.md)
- [Template variable](template-variable.md)
