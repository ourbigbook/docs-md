# Adding your first macro

↑ **Parent:** [Internals API](internals-api.md)

To add your own macro, try to copy from another existing macro that feels the closest in functionality.

For example, suppose we want something similar to [line break](line-break.md). So let's grep:

```
git grep '\bbr\b'
```

Grep currently gives:

```
index.js:8018:    'br',
index.js:8841:        'br': function(ast, context) { return '<br>' },
index.js:9792:        'br': function(ast, context) { return '\n'; },
index.js:10289:        'br': ourbigbookConvertSimpleElem,
test_bigb_output.bigb:71:br:
test_bigb_output.bigb:74:aa\br
test_bigb_output.bigb:75:bb\br
test_bigb_output.bigb:79:asdf\br
test_bigb_output.bigb:98:Non-br macro without arguments\i
```

All functionality is contained in [index.js](_file/index.js.md) as expected. Expanding the hits a but further we see:


```
const DEFAULT_MACRO_LIST = [
  new Macro(
    'br',
    [],
    {
      phrasing: true,
    }
  ),

const OUTPUT_FORMATS_LIST = [

  new OutputFormat(
    OUTPUT_FORMAT_HTML,
      ext: HTML_EXT,
      convert_funcs: {
        'br': function(ast, context) { return '<br>' },

    OUTPUT_FORMAT_ID,
    {
      ext: 'id',
      convert_funcs: {
        'br': function(ast, context) { return '\n'; },

  new OutputFormat(
    OUTPUT_FORMAT_OURBIGBOOK,
    {
      ext: OURBIGBOOK_EXT,
      convert_funcs: {
        'br': ourbigbookConvertSimpleElem,
```
so it should be quick direct to see what is going on from this.

## ↑ Ancestors (3)

1. [Internals API](internals-api.md)
2. [Developing OurBigBook](developing-ourbigbook.md)
3. [OurBigBook Project](split.md)
