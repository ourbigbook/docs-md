# Wikibot LLM body population

↑ **Parent:** [Wikipedia bot](wikipedia-bot.md)

Mostly for fun we've populated the body of wikibot-generated sections on [OurBigBook.com](ourbigbook-com.md) with some LLM-generated content.

At first we considered using Ollama with something like llama3.2, but because each prompt took 5 seconds on a laptop it would take about 5 days to do all 100k articles and so we decided to try existing API providers.

We finally ended up going with the cheapest model that seemed easy to use and chose OpenAI gpt-4o-mini. We managed to complete the generation for 100 output tokens per section with only 3 dollars. To help reduce costs we also:
- used batch jobs, which can take up to 24 hours to complete and sometimes just fail after 24 hours
- enabled data collection to get some extra credits.

We just took the Wikipedia titles and prompted directly:
```
What is TITLE?
```

It is a bit of shame that many of the replies end in crap like "Let me know if you need more help on this subject"-type output. We could have prevented those with a role=system prompt, but there seems to be no way to factor out a single system prompt for multiple queries, so the input token could would have increased.

Our pipeline is as follows. First clone the wikibot repo:
```
cd ..
git clone https://github.com/ourbigbook/wikibot
cd -
```

Then:
```
export OPENAI_API_KEY=...
./wikibot-static-llm-submit

# Wait 24 hours and pray.
# Check completion with:
./wikibot-static-llm-list-batches

./wikibot-static-jsonl-to-sqlite
./wikibot-static-add-body
```
The generated repository with bodies added should now be present under:
```
_out/wikibot-llm/repo/
```

The key intermediate file `oai_out.jsonl.zip` which contains the prompt outputs has been backed up to: [https://github.com/ourbigbook/ourbigbook-media/blob/master/oai_out.jsonl.zip](https://github.com/ourbigbook/ourbigbook-media/blob/master/oai_out.jsonl.zip)

## 🏷️ Tagged (1)

- [LLM-generated wikibot abstracts](news/llm-generated-wikibot-abstracts.md)

## ↑ Ancestors (5)

1. [Wikipedia bot](wikipedia-bot.md)
2. [Generated data](generated-data.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [LLM-generated wikibot abstracts](news/llm-generated-wikibot-abstracts.md)
