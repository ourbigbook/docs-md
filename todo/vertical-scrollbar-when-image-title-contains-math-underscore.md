# Vertical scrollbar when image title contains math underscore

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [CSS](css.md)

Only happens when the title would fit in a single line:
```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/BSD_data_plot_for_elliptic_curve_800h1.svg/960px-BSD_data_plot_for_elliptic_curve_800h1.svg.png]
{title=$a_b$}
{height=400}
```

For long titles that go over a single line, it doesn't happen.

Removing from `ourbigbook.scss`:
```
figure {
  overflow-x: auto;
```
fixes for some reason, but breaks everything else, as it adds a global vertical scrollbar to the page if there are any images wider than it (when above the mobile mode where images are just width 100%.

The fundamental issue seems to be: [https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue](https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue) which we don't know how to work around. Omg.

To get a clearer effect edit ourbigbook.scss to:
```
.katex { font-size: 20.2em; }
```
Only the separation between `a` and its subscript `b` seems to matter.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
