# Remove the path parameter from the article creation API

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md)

<a id="_283"></a>
Edit: a use case has come up for this: if we can find an existing article that the user is trying to update, we might be able to determine that it does not need to be converted in the first place: [skip re-render from API if article was unchanged](skip-re-render-from-api-if-article-was-unchanged.md). But then of course we can't render the article to find its ID, as the hole point is to skip that render in the first place.

<a id="_284"></a>
We likely want to get rid of the `path` parameter, and instead determine IDs fully from more "in-band" things like `{id}` and `{scope}`.

<a id="_285"></a>
Both `{scope}` for subdirs and `{id}` for custom id basename !== from title should already be working, we just haven't setup ourbigbook CLI to inject `{id}` based on file path I think.

<a id="_286"></a>
`{scope}` is however not really usable in general on the same source tree of cirosantilli.github.io due to [https://github.com/ourbigbook/ourbigbook/issues/284](https://github.com/ourbigbook/ourbigbook/issues/284).

<a id="_287"></a>
This would forbid some constructs that are currently possible locally, e.g. scopes that are not children such as:

<a id="_288"></a>
parent.bigb<a id="_289"></a>

```
= Parent

== Child
{scope}

=== Child 2
{scope}
```

<a id="_290"></a>
parent2.bigb<a id="_291"></a>

```
= Parent

\Include[child/subdir]
```

<a id="_292"></a>
child/subdir.bigb<a id="_293"></a>

```
= Subdir
```

<a id="_294"></a>
but that is fine, it is saner if we enforce scopes to match the tree article tree hierarchy.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
