# At mention and topics locally

↑ **Parent:** [Issues](issues.md)  
🏷️ **Tags:** [Web](web.md)

<a id="_156"></a>
The constructs from [at mention and topics on web](at-mention-and-topics-on-web.md) should also just work locally, and redirect to ourbigbook.com by default.

<a id="_157"></a>
Once they work, document them with something like:

<a id="_158"></a>
```
= `\x` `href` argument
{parent=`\x` sargument}

If the `href` argument starts with certain prefixes, magic links are generated:
* `@`: link to <OurBigBook.com> user profiles, e.g.:
  \OurBigBookExample[[
  I love \a[@cirosantilli], he is great!
  ]]
  links to: https://ourbigbook.com/cirosantilli

  TODO make it work without the `\a`, just: `@cirosantilli`.
* `#`: link to <OurBigBook.com> <OurBigBook Web topics>[topics]:
  \OurBigBookExample[[
  \a[#quantum-mechanics][Quantum mechanics] is very difficult to understand.
  ]]
  links to: https://ourbigbook.com/go/topic/quantum-mechanics
```

<a id="_159"></a>
It is not perfectly elegant to use `<>` for this, especially locally, since it means linking to IDs that don't exist (on Web, `@username` is an actually regular ID on the DB. But `#topic` isn't). But perhaps just having the `<>` links to non-files is just the way to go.

## ↑ Ancestors (3)

1. [Issues](issues.md)
2. [TODO](../todo-split.md)
3. [OurBigBook Project](../split.md)
