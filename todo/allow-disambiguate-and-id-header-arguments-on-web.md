# Allow disambiguate and id header arguments on web

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Scope](scope.md), [Web](web.md)

<a id="_383"></a>
Currently these do not affect the article's ID as there is a fundamental limitation of the `convert` function, which determines the "file path" based solely on the title content, and ignores the title arguments such as `disambiguate`. The ID of the first header, the toplevel ID, then just gets fixed to that (as is meant to happen, first toplevel gets Id fixed), ignoring `disambiguate`.

<a id="_384"></a>
This is worked around on web upload by passing the `id` as the `path` explicitly as an argument. But this argument is not available on web UI, and it would be ugly anyways, what we want is for it to "just work" by default without the user having to explicitly set an ID on web UI.

<a id="_385"></a>
Fixed at: 56e8d17aa1b716ce69689c6b8aaae0acf4804421 web: fix editing for articles with ID modifiers like scope or disambiguate

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
