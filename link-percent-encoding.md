# Link percent encoding

↑ **Parent:** [Link](link.md)

[OurBigBook](split.md) automatically encodes all link `href` for characters that are not recommended for URLs.

This way you can for example simply write arbitrary Unicode URLs and OurBigBook will escape them for you on the HTML output.

The only exception for this is the percent sign itself `%`, which it leaves untouched so that explicitly encoded URLs also work. So if you want a literal percent then you have to explicitly write it yourself as `%25`.


```
* acute a Á as raw Unicode: https://en.wikipedia.org/wiki/Á
* acute a Á explicitly escaped by user: https://en.wikipedia.org/wiki/%C3%81
```
which renders as:



> 
> - acute a Á as raw Unicode: [https://en.wikipedia.org/wiki/Á](https://en.wikipedia.org/wiki/Á)
> - acute a Á explicitly escaped by user: [https://en.wikipedia.org/wiki/%C3%81](https://en.wikipedia.org/wiki/%C3%81)

## ↑ Ancestors (4)

1. [Link](link.md)
2. [Macro](macro.md)
3. [OurBigBook Markup](ourbigbook-markup.md)
4. [OurBigBook Project](split.md)
