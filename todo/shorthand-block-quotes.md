# Shorthand block quotes

↑ **Parent:** [Closed issues](closed-issues.md)  
🏷️ **Tags:** [Web](web.md)

<a id="_412"></a>
OK, I need that, let's go. `__` like Asciidoctor?<a id="_413"></a>

```
Before.

__
In quote

Another paragraph.
__

After
```

<a id="_414"></a>
Maybe also just add inline (non-block) quotes now?

<a id="_415"></a>
We could also consider an indent based method:<a id="_416"></a>

```
> In quote

  Another paragraph.

After
```

<a id="_417"></a>
The cool thing about that is that it would save the sweet sweet one liners:<a id="_418"></a>

```
Before

> In quote

After
```
but meh, too much indentation typing I think.

<a id="_419"></a>
Prototype implemented on branch `insane-quote` with just the single underscore `_` version to make it fully symmetric with code/math, which is easier to implement. Just by running the tests we saw some common conflicts with the single `_` due to it appearing in some local file paths pieces of URLs, e.g.:<a id="_420"></a>

```
= My topic
{wiki=Another_one}
```
and:<a id="_421"></a>

```
= Notindex

<file/path/to/my_file.jpg>

== path/to/my_file.jpg
{file}
```
Some ideas:<a id="_422"></a>

<a id="_423"></a>
- generalize things a bit so that `_` does not exist. Inline quotes go just with the usual `""` ascii art
<a id="_424"></a>
- make some arguments literal by default to cover those common cases. Makes language a bit more insane, but perhaps it is for the best, we don't want HTML expanding in anything that won't end up in the HTML right. That makes the possible future case of defining variables a bit harder. But we could overcome it by just making literals be non literals then when literal is the default, e.g.:<a id="_425"></a>

  ```
  = My topic
  {wiki=Another_one}

  = My topic
  {{wiki=\somevar}}
  ```

<a id="_426"></a>
Hmm, going with `>` finally. Part of the reason being that for multiline quotes: `\Q[]` is just saner and same number of characters. But for single line quotes, `>` is just too sweet.

## ↑ Ancestors (3)

1. [Closed issues](closed-issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
