# Remove scope from toc entry IDs

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [CLI](cli.md), [Scope](scope.md)

<a id="_388"></a>
Happens on CLI and Web, though the web one is a bit artificial.

<a id="_389"></a>
E.g. [https://cirosantilli.com/x86-paging#toc-x86-paging/sample-code](https://cirosantilli.com/x86-paging#toc-x86-paging/sample-code) should instead be just: [https://cirosantilli.com/x86-paging#toc-sample-code](https://cirosantilli.com/x86-paging#toc-sample-code). Links from headers to currently work however.

<a id="_390"></a>
On web will require extra caution after we decided to initially stop culling scopes: [missing header metadata such as like button, same topic and issue link on headers under a scope](missing-header-metadata-such-as-like-button-same-topic-and-issue-link-on-headers-under-a-scope.md).

<a id="_391"></a>
Edit: this was fixed on web after we did the insane and amazing dynamic tree JavaScript redirects: [https://ourbigbook.com/cirosantilli/x86-paging#_toc/sample-code](https://ourbigbook.com/cirosantilli/x86-paging#_toc/sample-code) But we never got round to fixing it on static where it still goes to the bad [https://cirosantilli.com/x86-paging#_toc/x86-paging/sample-code](https://cirosantilli.com/x86-paging#_toc/x86-paging/sample-code)

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
