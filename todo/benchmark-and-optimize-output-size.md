# Benchmark and optimize output size

↑ **Parent:** [Closed issues](closed-issues.md)

Test repo source code size during tests: 7.2 MiB

Full ToC removal with hack:
```
 function renderTocFromEntryList({ add_test_instrumentation, entry_list, descendant_count_html, tocIdPrefix }) {
+  return ''
```
Test repo output size: 166.6 MB -\> 114.2 MB, so ToC was 31 %

Let's check header knockout with:
```
        [Macro.HEADER_MACRO_NAME]: function(ast, context, opts={}) {
          return ''
```
down to 151.7 MiB, so headers were about 9%.

And finally removing the toplevel stuff:
```
       toplevel_child_modifier: function(ast, context, out) {
+        return 'out'
```
down to 161.8 MB, so these were only about 3%.

These should be the only bulk things we have really, everything else will likely be much harder to get wrong.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
