# OurBigBook Web hide article dates

↑ **Parent:** [OurBigBook Web user manual](ourbigbook-web-user-manual.md)

By default, when you publish on [OurBigBook Web](ourbigbook-web.md), either via the [web editor](web-editor.md) or via [Web upload](web.md) from the command line, the server will store and display the date at which articles were created and updated.

To prevent that, you can set the "Hide article dates" user option, which prevents storage of such information on the database entirely.

This makes [OurBigBook Web](ourbigbook-web.md) behave a little more like [static websites](p-publish.md), where the publish date is only shown if you explicitly set it for the article with the [`\H` `created` argument](h-created-argument.md) or [`\H` `updated` argument](h-updated-argument.md).

When articles are created or updated with this option is selected, articles created will always appear last when listing articles by newest or latest.

## ↑ Ancestors (3)

1. [OurBigBook Web user manual](ourbigbook-web-user-manual.md)
2. [OurBigBook Web](ourbigbook-web.md)
3. [OurBigBook Project](split.md)
