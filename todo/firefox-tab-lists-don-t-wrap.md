<h1 id="firefox-tab-lists-don-t-wrap">Firefox tab lists don't wrap</h1>

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Firefox](firefox.md), [Web](web.md)

<a id="_133"></a>
On Firefox 109, tab lists such as those in the home page don't wrap if the screen is narrow.

<a id="_134"></a>
This is due to:<a id="_135"></a>

```
.tab-item: { white-space: pre }
```
but does not make much sense, as it should only take effect inside `.tab-item`, not on the `.tab-list` itself, feels like a firefox bug.

<a id="_136"></a>
We want the `white-space: pre` so that tab entries won't be broken up across lines.

<a id="_137"></a>
Works fine in Chromium 109.

<a id="_138"></a>
TODO can't reproduce on a minimal HTML page, so anoying!!!<a id="_139"></a>

```
<!doctype html>
<html lang=en>
<head>
<meta charset=utf-8>
<title>Min sane</title>
<style>
span {
  white-space: pre;
}
</style>
</head>
<body>
  <span>My item 1</span>
  <span>My item 2</span>
  <span>My item 3</span>
  <span>My item 4</span>
  <span>My item 5</span>
  <span>My item 6</span>
  <span>My item 7</span>
  <span>My item 8</span>
  <span>My item 9</span>
  <span>My item 10</span>
  <span>My item 11</span>
  <span>My item 12</span>
  <span>My item 13</span>
  <span>My item 14</span>
  <span>My item 15</span>
  <span>My item 16</span>
  <span>My item 17</span>
  <span>My item 18</span>
  <span>My item 19</span>
</body>
</html>
```

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
