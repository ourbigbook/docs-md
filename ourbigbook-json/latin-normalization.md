<h1 id="ourbigbook-json/latin-normalization">Latin normalization</h1>

↑ **Parent:** [`Id` `normalize` `latin`](id-normalize-latin.md)

<a id="ourbigbook-json/_3773"></a>
ASCII normalization is a custom OurBigBook defined normalization that converts many characters that look like Latin characters into Latin characters.

<a id="ourbigbook-json/_3774"></a>
For now, we are using the `deburr` method of Lodash: [https://lodash.com/docs/4.17.15#deburr](https://lodash.com/docs/4.17.15#deburr), which only affects Latin-like characters.

<a id="ourbigbook-json/_3775"></a>
In addition to `deburr` we also convert:<a id="ourbigbook-json/_3776"></a>

<a id="ourbigbook-json/_3777"></a>
- en-dash and em-dash to simple ASCII dash `-`. Wikipedia Loves en-dashes in their article titles!
<a id="ourbigbook-json/_3778"></a>
- greek letters are replaced with their standard latin names, e.g. `α` to `alpha`

<a id="ourbigbook-json/_3779"></a>
One notable effect is that it converts variants of ASCII letters to ASCII letters. E.g. `é` to `e` removing the accent.

<a id="ourbigbook-json/_3780"></a>
This operation is kind of a superset of Unicode normalization acting only on Latin-like characters, where Unicode basically only removes things like diacritics.

<a id="ourbigbook-json/_3781"></a>
OurBigBook normalization on the other also does other natural transformations that Unicode does not do, e.g. `æ` to `ae` as encoded by `deburr` and further custom replacements.

<a id="ourbigbook-json/_3782"></a>
TODO `lodash.deburr`:<a id="ourbigbook-json/_3783"></a>

<a id="ourbigbook-json/_3784"></a>
- only deals with Unicode blocks "[Latin-1 Supplement](https://en.wikipedia.org/wiki/Latin-1_Supplement)" and "[Latin Extended-A](https://en.wikipedia.org/wiki/Latin_Extended-B)", notably missing [Latin Extended-B](https://en.wikipedia.org/wiki/Latin_Extended-B), [C](https://en.wikipedia.org/wiki/Latin_Extended-C) and [D](https://en.wikipedia.org/wiki/Latin_Extended-D), which contain some important characters. Pull requests have been ignored:<a id="ourbigbook-json/_3785"></a>

  <a id="ourbigbook-json/_3786"></a>
  - [https://github.com/lodash/lodash/issues/4530](https://github.com/lodash/lodash/issues/4530)
  <a id="ourbigbook-json/_3787"></a>
  - [https://github.com/lodash/lodash/pull/5491](https://github.com/lodash/lodash/pull/5491)

  so maybe we should just code our own on top.
<a id="ourbigbook-json/_3788"></a>
- misses some candidates in [letterlike symbols](https://en.wikipedia.org/wiki/Letterlike_Symbols)
<a id="ourbigbook-json/_3789"></a>
- [mathematical operators block](https://en.wikipedia.org/wiki/Mathematical_operators_and_symbols_in_Unicode#Mathematical_Operators_block)

<a id="ourbigbook-json/_3790"></a>
Bibliography:<a id="ourbigbook-json/_3791"></a>

<a id="ourbigbook-json/_3792"></a>
- [https://stackoverflow.com/questions/990904/remove-accents-diacritics-in-a-string-in-javascript](https://stackoverflow.com/questions/990904/remove-accents-diacritics-in-a-string-in-javascript)
<a id="ourbigbook-json/_3793"></a>
- [https://github.com/ourbigbook/ourbigbook/issues/162](https://github.com/ourbigbook/ourbigbook/issues/162)

## ↑ Ancestors (5)

1. [`Id` `normalize` `latin`](id-normalize-latin.md)
2. [`Ourbigbook.json` `id`](id.md)
3. [`Ourbigbook.json`](../ourbigbook-json.md)
4. [OurBigBook CLI](../ourbigbook-cli.md)
5. [OurBigBook Project](../split.md)

## ← Incoming links (2)

- [Automatic ID from title](../automatic-id-from-title.md)
- [`Id` `normalize` `latin`](id-normalize-latin.md)
