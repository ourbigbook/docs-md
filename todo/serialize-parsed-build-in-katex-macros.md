# Serialize parsed build-in KaTeX macros

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Math](math.md)

<a id="_178"></a>
I.e. save the output of `katex.renderToString` to JSON or some other format. This approach would ensure minimal load times no matter what KaTeX is doing, and possibly provide some good portability.

<a id="_179"></a>
Off the bat `JSON.stringify` doesn't work due to circular references though that can be overcome: [https://stackoverflow.com/questions/10392293/stringify-convert-to-json-a-javascript-object-with-circular-reference](https://stackoverflow.com/questions/10392293/stringify-convert-to-json-a-javascript-object-with-circular-reference)

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
