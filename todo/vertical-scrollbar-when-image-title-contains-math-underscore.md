# Vertical scrollbar when image title contains math underscore

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [CSS](css.md)

<a id="_473"></a>
Only happens when the title would fit in a single line:<a id="_474"></a>

```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/BSD_data_plot_for_elliptic_curve_800h1.svg/640px-BSD_data_plot_for_elliptic_curve_800h1.svg.png]
{title=$a_b$}
{height=400}
```

<a id="_475"></a>
For long titles that go over a single line, it doesn't happen.

<a id="_476"></a>
Removing from `ourbigbook.scss`:<a id="_477"></a>

```
figure {
  overflow-x: auto;
```
fixes for some reason, but breaks everything else, as it adds a global vertical scrollbar to the page if there are any images wider than it (when above the mobile mode where images are just width 100%.

<a id="_478"></a>
The fundamental issue seems to be: [https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue](https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue) which we don't know how to work around. Omg.

<a id="_479"></a>
To get a clearer effect edit ourbigbook.scss to:<a id="_480"></a>

```
.katex { font-size: 20.2em; }
```
Only the separation between `a` and its subscript `b` seems to matter.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
