<h1 id="no-web-nested-set-bulk"><code>--no-web-nested-set-bulk</code></h1>

↑ **Parent:** [OurBigBook CLI options](ourbigbook-cli-options.md)

Update the [nested set](nested-set.md) after each article, rather than just once after all articles have been uploaded.

There is a complex time tradeoff between using this option or not, which depends on:
- how many articles the user has
- how many articles are being uploaded

This option was initially introduced for [Wikipedia bot](wikipedia-bot.md) uploads. At 104k articles, the bulk update takes 1 minute, but each individual update of an empty article takes about 6 seconds (and is dominated by the nested set update time), making this option an indispensable time saver for the initial upload in that case

Therefore in that case, for less than 10 articles you are better off without this option. But with more thatn 10 articles you would want to use it.

This rule of thumb should scale for smaller deployments as well however. E.g. at 10k articles, both individual updates and bulk updates should be 10x faster, so the "use this option for 10 or more articles" rule of thumb should still be reasonable.

## ↑ Ancestors (3)

1. [OurBigBook CLI options](ourbigbook-cli-options.md)
2. [OurBigBook CLI](ourbigbook-cli.md)
3. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Wikipedia bot](wikipedia-bot.md)
