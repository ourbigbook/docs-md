# Benchmark and optimize output size

↑ **Parent:** [Closed issues](closed-issues.md)

<a id="_449"></a>
Test repo source code size during tests: 7.2 MiB

<a id="_450"></a>
Full ToC removal with hack:<a id="_451"></a>

```
 function renderTocFromEntryList({ add_test_instrumentation, entry_list, descendant_count_html, tocIdPrefix }) {
+  return ''
```
Test repo output size: 166.6 MB -\> 114.2 MB, so ToC was 31 %

<a id="_452"></a>
Let's check header knockout with:<a id="_453"></a>

```
        [Macro.HEADER_MACRO_NAME]: function(ast, context, opts={}) {
          return ''
```
down to 151.7 MiB, so headers were about 9%.

<a id="_454"></a>
And finally removing the toplevel stuff:<a id="_455"></a>

```
       toplevel_child_modifier: function(ast, context, out) {
+        return 'out'
```
down to 161.8 MB, so these were only about 3%.

<a id="_456"></a>
These should be the only bulk things we have really, everything else will likely be much harder to get wrong.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
