# News

↑ **Parent:** [Publicity](README.md#publicity)

<a id="_1"></a>
This is a list of project announcements such as new features sorted in chronological order, from the newest to oldest.

<a id="_2"></a>
Significant entries will have a corresponding announcement on the following [official accounts](README.md#official-accounts):<a id="_3"></a>

<a id="_4"></a>
- [https://mastodon.social/@OurBigBook](https://mastodon.social/@OurBigBook)
<a id="_5"></a>
- [https://twitter.com/OurBigBook](https://twitter.com/OurBigBook)
<a id="_6"></a>
- [https://www.linkedin.com/company/ourbigbook](https://www.linkedin.com/company/ourbigbook)
<a id="_7"></a>
- [https://www.facebook.com/OurBigBook](https://www.facebook.com/OurBigBook)
<a id="_8"></a>
- [https://www.instagram.com/ourbigbook](https://www.instagram.com/ourbigbook)

**Table of contents**

- [File upload on Web](#file-upload-on-web)
- [LLM-generated wikibot abstracts](#llm-generated-wikibot-abstracts)
- [Automatic topic linking](#automatic-topic-linking)
- [Signup IP blacklist, VPN detection and account locking](#signup-ip-blacklist-vpn-detection-and-account-locking)
- [Web searches find words inside title on PostgreSQL](#web-searches-find-words-inside-title-on-postgresql)
- [Article announcement](#article-announcement)
- [Web navigation two level tab cleanup](#web-navigation-two-level-tab-cleanup)
- [Scope ancestors show on toplevel header and page title](#scope-ancestors-show-on-toplevel-header-and-page-title)
- [Topic ID shows on web editor when creating a new article](#topic-id-shows-on-web-editor-when-creating-a-new-article)
- [Create new articles from table of contents](#create-new-articles-from-table-of-contents)
- [Profile picture upload](#profile-picture-upload)
- [Disambiguate shows on navigation](#disambiguate-shows-on-navigation)
- [Tagged articles and other article lists added to Web](#tagged-articles-and-other-article-lists-added-to-web)
- [Static ToC search](#static-toc-search)
- [Article and topic ID prefix search](#article-and-topic-id-prefix-search)
- [Tagged headers show under non-toplevel headers](#tagged-headers-show-under-non-toplevel-headers)
- [OurBigBook CLI enforces consistent header tree by default](#ourbigbook-cli-enforces-consistent-header-tree-by-default)
- [ourbigbook.com/cirosantilli loads 2x as fast after database optimizations](#ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations)
- [Visual Studio Code extension overhaul](#visual-studio-code-extension-overhaul)
- [Body preview on all article lists](#body-preview-on-all-article-lists)
- [Unlisted articles on web](#unlisted-articles-on-web)
- [A few articles in same topic are shown at the bottom of every article page](#a-few-articles-in-same-topic-are-shown-at-the-bottom-of-every-article-page)
- [Short URL fragments on OurBigBook Web](#short-url-fragments-on-ourbigbook-web)
- [`\Hr` horizontal rule macro created](#hr-horizontal-rule-macro-created)
- [Gray on gray color replaces green on black and many other CSS improvements](#gray-on-gray-color-replaces-green-on-black-and-many-other-css-improvements)
- [Intro to OurBigBook video](#intro-to-ourbigbook-video)
- [Pinned article](#pinned-article)
- [Automatically create `_file` pages for every file](#automatically-create-file-pages-for-every-file)
- [Always show large text files on `_file` split headers](#always-show-large-text-files-on-file-split-headers)
- [Optimize generated HTML size by adding on-the-fly elements](#optimize-generated-html-size-by-adding-on-the-fly-elements)
- [Suggest article creation for topics that don't exist](#suggest-article-creation-for-topics-that-don-t-exist)

## File upload on Web

↑ **Parent:** [News](news.md)

<a id="_9"></a>
It is now possible to have create file uploads on [OurBigBook Web](README.md#ourbigbook-web), e.g.:<a id="_10"></a>

<a id="_11"></a>
- [https://ourbigbook.com/cirosantilli/_dir](https://ourbigbook.com/cirosantilli/_dir)
<a id="_12"></a>
- [https://ourbigbook.com/cirosantilli/_dir/c](https://ourbigbook.com/cirosantilli/_dir/c)
<a id="_13"></a>
- [https://ourbigbook.com/cirosantilli/_raw/c/segfault.c](https://ourbigbook.com/cirosantilli/_raw/c/segfault.c)
You can upload images, source code, or any other type of file.

<a id="_14"></a>
Previously, you'd just get broken links when publishing to [OurBigBook Web](README.md#ourbigbook-web) if you linked to your files with the [`\a` macro](README.md#link) or other related constructs.

<a id="_15"></a>
The implementation attempts to follow what already existed for [static websites](README.md#p-publish) as closely as possible.

<a id="_16"></a>
The current implementation has a few limitations which should be fixed one day:<a id="_17"></a>

<a id="_18"></a>
- there is no web UI for file upload, it is exposed via CLI only
<a id="_19"></a>
- file previews don't show under corresponding `_file` articles as they do on static
<a id="_20"></a>
- `_file` articles are not properly auto-generated for files that don's have explicit articles, we just show `_raw` under `_file`

<a id="image-user-home-pages-have-a-link-to-the-root-file-directory-of-the-user"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/user-page-arrow.png" alt="" height="536">

**[Figure 1](#image-user-home-pages-have-a-link-to-the-root-file-directory-of-the-user). User home pages have a link to the root file directory of the user**. [Source](https://ourbigbook.com/cirosantilli).

<a id="image-sample-directory-listing"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/directory-listing.png" alt="" height="533">

**[Figure 2](#image-sample-directory-listing). Sample directory listing**. [Source](https://ourbigbook.com/cirosantilli/\_dir/c).

<a id="image-sample-raw-listing"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-files/raw.png" alt="" height="153">

**[Figure 3](#image-sample-raw-listing). Sample raw listing**. [Source](https://ourbigbook.com/cirosantilli/\_file/c/segfault.c).

<a id="_21"></a>
Announced at:<a id="_22"></a>

<a id="_23"></a>
- [https://mastodon.social/@ourbigbook/114851233133955275](https://mastodon.social/@ourbigbook/114851233133955275)
<a id="_24"></a>
- [https://x.com/OurBigBook/status/1944713518474744230](https://x.com/OurBigBook/status/1944713518474744230)
<a id="_25"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7350479547579961347](https://www.linkedin.com/feed/update/urn:li:ugcPost:7350479547579961347)
<a id="_26"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid02AH8MfRBf4Dc3LzoeGPnZkKp9GffS8qr2hF4FoqC9g1eq1EcGHV1ABcFiPniF4pual](https://www.facebook.com/OurBigBook/posts/pfbid02AH8MfRBf4Dc3LzoeGPnZkKp9GffS8qr2hF4FoqC9g1eq1EcGHV1ABcFiPniF4pual)

## LLM-generated [wikibot](README.md#wikipedia-bot) abstracts

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Wikibot LLM body population](README.md#wikibot-llm-body-population)

<a id="_28"></a>
We've used gpt-4o-mini to automatically populate the 100k+ [wikibot](README.md#wikipedia-bot) articles. The process is described at: [Section "Wikibot LLM body population"](README.md#wikibot-llm-body-population). The entire generation was completed for only $3.

<a id="_29"></a>
Some of the abstracts can be seen e.g. under Wikibot's user page: [https://ourbigbook.com/wikibot#mathematics](https://ourbigbook.com/wikibot#mathematics) or under specific topics such as: [https://ourbigbook.com/go/topic/qijue](https://ourbigbook.com/go/topic/qijue)

<a id="_30"></a>
We've limited the output to 100 tokens each, and for each topic X simply queried"<a id="_31"></a>

```
What is X?
```

<a id="_32"></a>
Unfortunately there is quite a bit of "obviously LLM generated trash" in those. Some of it we sedded out, but some stray markdown and lists with a single item cut short due to the 100 token limit remain.

<a id="_33"></a>
This was mostly for fun, but it might sometimes serve as a good quick definition on previously empty [topic](README.md#ourbigbook-web-topics) pages and articles on the same topic under a given article.

<a id="_34"></a>
Hopefully it will also kick some of our pages out of Google's "Soft 404" limbo; pages that it refuses to index because they seem empty and it considers them as being essentially 404s, inexistent pages, and bring in some tail end traffic for the more niche subjects.

<a id="_35"></a>
[Automatic topic linking](#automatic-topic-linking) is also active on these as everywhere else on the site, which ends up interlinking everything automatically.

<a id="image-wikibot-autogenerated-abstract-showing-on-its-topic-page"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/wikibot/topic.png" alt="" height="732">

**[Figure 4](#image-wikibot-autogenerated-abstract-showing-on-its-topic-page). Wikibot autogenerated abstract showing on its topic page**. [Source](https://ourbigbook.com/wikibot/qijue).

<a id="image-wikibot-autogenerated-abstracts-showing-on-the-wikibot-homepage"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/wikibot/home-scroll.png" alt="" height="683">

**[Figure 5](#image-wikibot-autogenerated-abstracts-showing-on-the-wikibot-homepage). Wikibot autogenerated abstracts showing on the Wikibot homepage**. [Source](https://ourbigbook.com/wikibot\#mathematics).

<a id="_36"></a>
Announced at:<a id="_37"></a>

<a id="_38"></a>
- [https://mastodon.social/@ourbigbook/114692187180281143](https://mastodon.social/@ourbigbook/114692187180281143)
<a id="_39"></a>
- [https://x.com/OurBigBook/status/1934534494834274759](https://x.com/OurBigBook/status/1934534494834274759)
<a id="_40"></a>
- [https://www.linkedin.com/feed/update/urn:li:activity:7340300952983203842/](https://www.linkedin.com/feed/update/urn:li:activity:7340300952983203842/)
<a id="_41"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid0oYpPGYe4ZzpKTtpcSSzui8f6DdjxUc9PCgwKeR6uHzw4py1tp5QJwQavPVuUMqekl](https://www.facebook.com/OurBigBook/posts/pfbid0oYpPGYe4ZzpKTtpcSSzui8f6DdjxUc9PCgwKeR6uHzw4py1tp5QJwQavPVuUMqekl)

## Automatic topic linking

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Automatic topic linking](#automatic-topic-linking)

<a id="_43"></a>
With [Automatic topic linking](README.md#automatic-topic-linking), regular text gets automatically converted to links to topics if part of the text matches an existing topic.

<a id="image-automatic-topic-linking-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics/automatic-link.png" alt="" height="1181">

**[Figure 6](#image-automatic-topic-linking-demo). Automatic topic linking demo**. [Source](https://ourbigbook.com/cirosantilli/things-that-i-like).

<a id="_44"></a>
Announcements:<a id="_45"></a>

<a id="_46"></a>
- [https://mastodon.social/@ourbigbook/114354907198101376](https://mastodon.social/@ourbigbook/114354907198101376)
<a id="_47"></a>
- [https://x.com/OurBigBook/status/1912948677569876379](https://x.com/OurBigBook/status/1912948677569876379)
<a id="_48"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7318714530119766018/](https://www.linkedin.com/feed/update/urn:li:share:7318714530119766018/)
<a id="_49"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid02ieBUqbNGV45hNQFtLjgmksgsEL1FJJ311j6ajBtYmeSPsTKUUMnXCMP7Df8XpJAml](https://www.facebook.com/OurBigBook/posts/pfbid02ieBUqbNGV45hNQFtLjgmksgsEL1FJJ311j6ajBtYmeSPsTKUUMnXCMP7Df8XpJAml)

## Signup IP blacklist, VPN detection and account locking

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Account locking](README.md#account-locking), [OurBigBook VPN blocking](README.md#ourbigbook-vpn-blocking), [OurBigBook Web signup IP blacklist](README.md#ourbigbook-web-signup-ip-blacklist), [`-W`, `--web`](README.md#web)

<a id="_54"></a>
As described at: [https://github.com/ourbigbook/ourbigbook/issues/346](https://github.com/ourbigbook/ourbigbook/issues/346), starting December 2024 and increasingly so through January and February 2025, [OurBigBook.com](README.md#ourbigbook-com) has been increasingly targeted by a SAPMmer group.

<a id="_55"></a>
About half of the SPAM posts were advertising cryptocurrency recovery services, but other scammy products were also advertized.

<a id="_56"></a>
They usually create a few posts every day, but they are very persistent and keep coming back day after day.

<a id="_57"></a>
The spammers were rather sophisticated:<a id="_58"></a>

<a id="_59"></a>
- almost always one SPAM post per account
<a id="_60"></a>
- all accounts use gmail addresses, presumably bought in bulk
<a id="_61"></a>
- the SPAMers use one of a variety of free VPN, most notably ExpressVPN, NordVPN and PIA

<a id="_62"></a>
At first we were rather amused that there would be human labor so cheap as to make such a work economically feasible.

<a id="_63"></a>
Adding SPAM to a website that has zero users and almost no views. Amazing!

<a id="_64"></a>
And it has to be manual work because the website is already protected by [OurBigBook Web reCAPTCHA setup](README.md#ourbigbook-web-recaptcha-setup).

<a id="_65"></a>
Furthermore all of the above strongly indicate a well organized SPAM operation that spams across a variety of websites for a variety of clients.

<a id="_66"></a>
But what really impressed us the most was [https://ourbigbook.com/alannakennedy/top-ways-to-recover-funds-from-cryptocurrency-scam-iforce-hacker-recovery](https://ourbigbook.com/alannakennedy/top-ways-to-recover-funds-from-cryptocurrency-scam-iforce-hacker-recovery) They actually upvoted a single post from 13 other accounts, making it by far the top article on [OurBigBook.com](README.md#ourbigbook-com) as visible at: [https://ourbigbook.com/go/articles?sort=score](https://ourbigbook.com/go/articles?sort=score)

<a id="image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/spam/crypto.png" alt="" height="971">

**[Figure 7](#image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com). Screenshot showing voting manipulated SPAM as the most highly upvoted article on OurBigBook.com**. [Source](https://web.archive.org/web/20250228110911/https://ourbigbook.com/go/articles?sort=score).

<a id="_67"></a>
Initially Ciro was debating to himself if he should allow this to continue or not. It is kind of fun to see them work and build a database of compromised gmail addresses.

<a id="_68"></a>
But finally, Ciro decided to put a stop to it mostly because:<a id="_69"></a>

<a id="_70"></a>
- they create so many accounts that it would take a lot of effort to go over all of them to decide which accounts are legit or not if in the future we wanted to nuke the SPAM accounts
<a id="_71"></a>
- manipulating the voting system was a step to far

<a id="_72"></a>
As a result, we have implemented the following features on the website, which should completely kill off this wave of SPAM, while hopefully having little impact to legitimate users:<a id="_73"></a>

<a id="_74"></a>
- [OurBigBook VPN blocking](README.md#ourbigbook-vpn-blocking): we now detect and forbid users from signing up from IPs of well known VPNs. The detection is done via API calls to [https://ipapi.is/](https://ipapi.is/) which allows fo 1000 free daily requests. We only make the requests after [reCAPTCHA](README.md#ourbigbook-web-recaptcha-setup), and if that service is ever down for some reason, we just skip the check instead
<a id="_75"></a>
- [OurBigBook Web signup IP blacklist](README.md#ourbigbook-web-signup-ip-blacklist): additionally, a small percentage of the SPAM was coming from Pakistani IPs which were not marked as part of a VPN. So we have also given the ability for admins to block some IPs manually to cover those
<a id="_76"></a>
- [Account locking](README.md#account-locking): for SPAM that goes through, we intend to use this new feature to [lock](README.md#account-locking) the SPAM accounts, which prevents them from further editing the database in any way, e.g. creating articles

<a id="_77"></a>
Furthermore, we will also use the pre-existing [unlisted](README.md#ourbigbook-web-unlisted-articles) article feature to unlist any particularly noisy spam such as the vote manipulated post.

<a id="_78"></a>
Announcements:<a id="_79"></a>

<a id="_80"></a>
- [https://mastodon.social/@ourbigbook/114081249345123512](https://mastodon.social/@ourbigbook/114081249345123512)
<a id="_81"></a>
- [https://x.com/OurBigBook/status/1895434750376165482](https://x.com/OurBigBook/status/1895434750376165482)
<a id="_82"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7301200741862420480](https://www.linkedin.com/feed/update/urn:li:share:7301200741862420480)
<a id="_83"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid0QPh3kRDe4bA99MpsVNEXX6LqURKooYMjWX3wC6phGrs2vv7PswyTs2GpwX3KTxUCl](https://www.facebook.com/OurBigBook/posts/pfbid0QPh3kRDe4bA99MpsVNEXX6LqURKooYMjWX3wC6phGrs2vv7PswyTs2GpwX3KTxUCl)

## Web searches find words inside title on PostgreSQL

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web PostgreSQL](README.md#ourbigbook-web-postgresql), [`-W`, `--web`](README.md#web)

<a id="_86"></a>
When searching articles and topics on [OurBigBook Web PostgreSQL](README.md#ourbigbook-web-postgresql), which is the case for [OurBigBook.com](README.md#ourbigbook-com):<a id="_87"></a>

<a id="_88"></a>
- each searched word can match exactly within any word of article [IDs](README.md#element-id)
<a id="_89"></a>
- the last word is considered as a prefix, and matches the start of any word of the ID
Previously, searches would only work if they were exactly a prefix of the title ID.

<a id="_90"></a>
For example, if you search:<a id="_91"></a>

```
calculus fun
```
then it will match titles such as:<a id="_92"></a>

```
Fundamental theorem of calculus
```
since it contains both:<a id="_93"></a>

<a id="_94"></a>
- the full word `calculus`
<a id="_95"></a>
- `fundamental` which contains the prefix `fun`

<a id="_96"></a>
This feature implemented efficiently by using PostgreSQL's built-in full text search module.

<a id="image-ourbigbook-web-search-highlighting-full-text-search"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/search/full-text-calculus-fun-arrow.png" alt="" height="738">

**[Figure 8](#image-ourbigbook-web-search-highlighting-full-text-search). OurBigBook Web search highlighting full text search**. [Source](https://ourbigbook.com/go/articles?body=false&search=calculus%20fun).

<a id="_97"></a>
Announcements:<a id="_98"></a>

<a id="_99"></a>
- [https://mastodon.social/@ourbigbook/114009281220745242](https://mastodon.social/@ourbigbook/114009281220745242)
<a id="_100"></a>
- [https://x.com/OurBigBook/status/1890828492222124218](https://x.com/OurBigBook/status/1890828492222124218)
<a id="_101"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7296594330725568512](https://www.linkedin.com/feed/update/urn:li:share:7296594330725568512)
<a id="_102"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid02oxfZ1kpfvPexovaEKqcE7D2MSEgQFM25ZdsQDXCLpV9C6uREKGNGV2A4E9MGuWi8l](https://www.facebook.com/OurBigBook/posts/pfbid02oxfZ1kpfvPexovaEKqcE7D2MSEgQFM25ZdsQDXCLpV9C6uREKGNGV2A4E9MGuWi8l)

## Article announcement

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Article announcement](#article-announcement), [`-W`, `--web`](README.md#web)

<a id="_105"></a>
It is now possible to send a link to one of your articles to all of your followers on [OurBigBook Web](README.md#ourbigbook-web) with the [Article announcement](README.md#article-announcement) feature. You can also add a short custom message to the announcement.

<a id="image-article-announcement-button-on-ourbigbook-web"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/announce/button-arrow.png" alt="" height="712">

**[Figure 9](#image-article-announcement-button-on-ourbigbook-web). Article announcement button on OurBigBook Web**. [Source](https://ourbigbook.com/cirosantilli/chain-rule).

<a id="image-modal-that-opens-up-after-clicking-the-article-announcement-button-on-ourbigbook-web"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/announce/modal.png" alt="" height="349">

**[Figure 10](#image-modal-that-opens-up-after-clicking-the-article-announcement-button-on-ourbigbook-web). Modal that opens up after clicking the article announcement button on OurBigBook Web**. [Source](https://ourbigbook.com/cirosantilli/chain-rule).

<a id="_106"></a>
Announced at:<a id="_107"></a>

<a id="_108"></a>
- [https://mastodon.social/@ourbigbook/113996648319817232](https://mastodon.social/@ourbigbook/113996648319817232)
<a id="_109"></a>
- [https://x.com/OurBigBook/status/1890019912057491534](https://x.com/OurBigBook/status/1890019912057491534)
<a id="_110"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7295785701730668544](https://www.linkedin.com/feed/update/urn:li:ugcPost:7295785701730668544)
<a id="_111"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid024djsou6JTQazqyALdejKL5g9TyfVdcEoc2j4pwsGeX49Sx7U2tJzPsfTkWstp2Twl](https://www.facebook.com/OurBigBook/posts/pfbid024djsou6JTQazqyALdejKL5g9TyfVdcEoc2j4pwsGeX49Sx7U2tJzPsfTkWstp2Twl)

## Web navigation two level tab cleanup

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_113"></a>
We have now cleaned up the tab navigation on [OurBigBook Web](README.md#ourbigbook-web) pages such as:<a id="_114"></a>

<a id="_115"></a>
- index page: [https://ourbigbook.com/](https://ourbigbook.com/)
<a id="_116"></a>
- user articles page: [https://ourbigbook.com/go/user/cirosantilli/articles](https://ourbigbook.com/go/user/cirosantilli/articles)
to have two levels organized by:<a id="_117"></a>

<a id="_118"></a>
- "object type" on the top row, e.g. articles, users, etc.
<a id="_119"></a>
- "further specifiers" on the bottom row, e.g. sorting and filtering

<a id="image-two-level-tab-navigation-on-ourbigbook-web"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-nav/articles-nobody-crop-arrow.png" alt="" height="451">

**[Figure 11](#image-two-level-tab-navigation-on-ourbigbook-web). Two-level tab navigation on OurBigBook Web**. [Source](https://ourbigbook.com/go/articles?body=false).

<a id="_120"></a>
Announced at:<a id="_121"></a>

<a id="_122"></a>
- [https://mastodon.social/@ourbigbook/113901029448917630](https://mastodon.social/@ourbigbook/113901029448917630)
<a id="_123"></a>
- [https://x.com/OurBigBook/status/1883900296394641470](https://x.com/OurBigBook/status/1883900296394641470)
<a id="_124"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7289667720843853824/](https://www.linkedin.com/feed/update/urn:li:share:7289667720843853824/)
<a id="_125"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid028oJXZnrThU7DWggysNVszptH6s31tsLp4qQ8xi2TPYATCEQcFvSTXmhqcYBBzY6tl](https://www.facebook.com/OurBigBook/posts/pfbid028oJXZnrThU7DWggysNVszptH6s31tsLp4qQ8xi2TPYATCEQcFvSTXmhqcYBBzY6tl)
<a id="_126"></a>
- [https://www.instagram.com/p/DFVaEhLtqP-/](https://www.instagram.com/p/DFVaEhLtqP-/)

## Scope ancestors show on toplevel header and page title

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Scope](README.md#h-scope-argument), [Static website](README.md#p-publish), [`-W`, `--web`](README.md#web)

<a id="_130"></a>
Starting now, if you have a [scoped](README.md#h-scope-argument) header such as `Sample code` in:<a id="_131"></a>

```
= x86 Paging
{scope}

== Sample code
```
then if you visit either the <a id="_132"></a>

<a id="_133"></a>
- [static website](README.md#p-publish): [https://cirosantilli.com/x86-paging/sample-code](https://cirosantilli.com/x86-paging/sample-code)
<a id="_134"></a>
- [dynamic website](README.md#ourbigbook-web): [https://ourbigbook.com/cirosantilli/x86-paging/sample-code](https://ourbigbook.com/cirosantilli/x86-paging/sample-code)
the title now shows something like:<a id="_135"></a>

```
x86 Paging / Sample code
```
instead of just:<a id="_136"></a>

```
Sample code
```
as before.

<a id="_137"></a>
This makes it easier to identify what scoped pages are about.

<a id="image-when-a-page-under-a-scope-is-at-toplevel-the-scope-prefix-is-clearly-shown"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/scope/h1-breadcrumb-arrow.png" alt="" height="499">

**[Figure 12](#image-when-a-page-under-a-scope-is-at-toplevel-the-scope-prefix-is-clearly-shown). When a page under a scope is at toplevel, the scope prefix is clearly shown**. [Source](https://ourbigbook.com/cirosantilli/x86-paging/sample-code).

<a id="_138"></a>
Announcements:<a id="_139"></a>

<a id="_140"></a>
- [https://mastodon.social/@ourbigbook/113883643054093455](https://mastodon.social/@ourbigbook/113883643054093455)
<a id="_141"></a>
- [https://x.com/OurBigBook/status/1882788838315340010](https://x.com/OurBigBook/status/1882788838315340010)
<a id="_142"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7288553515919003649](https://www.linkedin.com/feed/update/urn:li:share:7288553515919003649)
<a id="_143"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid0aWgAJwVdRgkBggDRZ9XVnowEHtUC9fFL769pCH5tXU8tX3dVXDFnNMLQCWK1m8hZl](https://www.facebook.com/OurBigBook/posts/pfbid0aWgAJwVdRgkBggDRZ9XVnowEHtUC9fFL769pCH5tXU8tX3dVXDFnNMLQCWK1m8hZl)
<a id="_144"></a>
- [https://www.instagram.com/p/DFNe62pt5Bj/](https://www.instagram.com/p/DFNe62pt5Bj/)

## Topic ID shows on web editor when creating a new article

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_146"></a>
This give a chance for users to see what else is present in that [topic](README.md#ourbigbook-web-topics) to better decide if it is a good fit for the article.

<a id="_147"></a>
Also, the topic ID now shows more clearly on each topic page to help users understand that each topic has its own ID that determines which articles will show up in the topic.

<a id="image-topic-link-showing-while-creating-a-new-article-on-the-web-editor"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/web-editor/topic-link-arrow.png" alt="" height="457">

**[Figure 13](#image-topic-link-showing-while-creating-a-new-article-on-the-web-editor). Topic link showing while creating a new article on the web editor**.

<a id="image-topic-id-showing-on-the-topic-page"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics/topic-id-arrow.png" alt="" height="500">

**[Figure 14](#image-topic-id-showing-on-the-topic-page). Topic ID showing on the topic page**.

<a id="_148"></a>
Announcements:<a id="_149"></a>

<a id="_150"></a>
- [https://mastodon.social/@ourbigbook/113866287091910918](https://mastodon.social/@ourbigbook/113866287091910918)
<a id="_151"></a>
- [https://x.com/OurBigBook/status/1881677047258652750](https://x.com/OurBigBook/status/1881677047258652750)
<a id="_152"></a>
- [https://www.linkedin.com/posts/ourbigbook_httpslnkdinefndixb4-the-topic-id-with-activity-7287442862936342530-MId9](https://www.linkedin.com/posts/ourbigbook_httpslnkdinefndixb4-the-topic-id-with-activity-7287442862936342530-MId9)
<a id="_153"></a>
- [https://www.instagram.com/p/DFFmInPtK1H/](https://www.instagram.com/p/DFFmInPtK1H/)

## Create new articles from table of contents

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_155"></a>
Previously, to create a new article that is a child or sibling of another article, you'd need to navigate to the article itself.

<a id="_156"></a>
Now you can also do it from the table of contents. This is an intuitive place to do it from, since you can browse the article tree and decide the best location to insert a new article from there.

<a id="image-you-can-add-a-new-article-under-or-after-another-on-ourbigbook-web-from-the-table-of-contents"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/new-from-toc/hover-arrow.png" alt="" height="694">

**[Figure 15](#image-you-can-add-a-new-article-under-or-after-another-on-ourbigbook-web-from-the-table-of-contents). You can add a new article under or after another on OurBigBook Web from the table of contents**.

<a id="image-after-clicking-the-plus-sign-a-popup-appears-that-allows-you-to-add-the-new-article"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/new-from-toc/modal.png" alt="" height="694">

**[Figure 16](#image-after-clicking-the-plus-sign-a-popup-appears-that-allows-you-to-add-the-new-article). After clicking the plus sign, a popup appears that allows you to add the new article**.

<a id="_157"></a>
Announcements:<a id="_158"></a>

<a id="_159"></a>
- [https://mastodon.social/@ourbigbook/113787046414438146](https://mastodon.social/@ourbigbook/113787046414438146)
<a id="_160"></a>
- [https://x.com/OurBigBook/status/1876605531516789030](https://x.com/OurBigBook/status/1876605531516789030)
<a id="_161"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7282371645292347392/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7282371645292347392/)
<a id="_162"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid0x1BzdnKuXgWn3jZwZrHj3Y2nofy9mFaJPwWKaZqqMzQYEnjqJboL8p8CgMvW4rxXl](https://www.facebook.com/OurBigBook/posts/pfbid0x1BzdnKuXgWn3jZwZrHj3Y2nofy9mFaJPwWKaZqqMzQYEnjqJboL8p8CgMvW4rxXl)
<a id="_163"></a>
- [https://www.instagram.com/p/DEhnnPttK8k](https://www.instagram.com/p/DEhnnPttK8k)

## Profile picture upload

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_165"></a>
You can now update your profile picture on [OurBigBook Web](README.md#ourbigbook-web) by uploading an image to the website like in a normal website.

<a id="_166"></a>
Previously, we only supported linking to an external image URL. Now this is not allowed anymore and you must instead upload your image to the website. Existing external links will continue to work, but if you want to update the profile picture again, then you will need to upload your own next time.

<a id="_167"></a>
Besides being a basic feature expected from any modern website, this is the first instance of "static file upload" on the site, and serves as part of a more general static file upload mechanism that can be later reused for other important features like uploading images for your articles.

<a id="_168"></a>
This initial implementation is very simplistic: we are just storing the image directly in the database. We will look into migrating to a more proper static file solution later on if this starts to hurt performance. We're using the [sharp](https://github.com/lovell/sharp) Node.js image processing library, a frontend to [libvips](https://github.com/libvips/libvips), to downsize input images as needed.

<a id="image-ourbigbook-web-profile-picture-upload"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/profile-picture/update-arrow.png" alt="" height="800">

**[Figure 17](#image-ourbigbook-web-profile-picture-upload). OurBigBook Web profile picture upload**. Clicking on the current profile picture opens up a file dialog which allows you to select an image from your computer to be your new profile picture.

<a id="_169"></a>
Announcements:<a id="_170"></a>

<a id="_171"></a>
- [https://x.com/OurBigBook/status/1868924960749826281](https://x.com/OurBigBook/status/1868924960749826281)
<a id="_172"></a>
- [https://mastodon.social/@ourbigbook/113667036536861645](https://mastodon.social/@ourbigbook/113667036536861645)
<a id="_173"></a>
- [https://www.linkedin.com/posts/ourbigbook_httpslnkdinexqfia-u-you-can-now-update-activity-7274690906065145856-1ho7/](https://www.linkedin.com/posts/ourbigbook_httpslnkdinexqfia-u-you-can-now-update-activity-7274690906065145856-1ho7/)

## Disambiguate shows on navigation

↑ **Parent:** [News](news.md)

<a id="_174"></a>
The [`\H` `disambiguate` argument](README.md#disambiguate-argument) now shows on most navigation locations including:<a id="_175"></a>

<a id="_176"></a>
- article indices on [`-W`, `--web`](README.md#web)
<a id="_177"></a>
- tagged/incoming article lists on [`-W`, `--web`](README.md#web) and [static](README.md#p-publish)
<a id="_178"></a>
- breadcrumb navigation on [`-W`, `--web`](README.md#web) and [static](README.md#p-publish)
This makes it easier to understand what the topic is about when [disambiguate](README.md#disambiguate-argument) is fundamental.

<a id="image-ourbigbook-web-tagged-article-list-with-disambiguate"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/disambiguate/tagged-classification-mathematics-arrow.png" alt="" height="818">

**[Figure 18](#image-ourbigbook-web-tagged-article-list-with-disambiguate). OurBigBook Web tagged article list with disambiguate**. <a id="_179"></a>
Live URL: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

<a id="_180"></a>
This change adds the "(mathematics)" disambiguate to "Classification (mathematics)", which makes the header much clearer than just "Classification".

---

<a id="_181"></a>
Announcements:<a id="_182"></a>

<a id="_183"></a>
- [https://x.com/OurBigBook/status/1868648997105422602](https://x.com/OurBigBook/status/1868648997105422602)
<a id="_184"></a>
- [https://mastodon.social/@ourbigbook/113662727590595159](https://mastodon.social/@ourbigbook/113662727590595159)

## Tagged articles and other article lists added to Web

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_186"></a>
For some time we have been listing certain ["cross article" metadata](README.md#header-metadata-section) at the bottom of articles on both [`-W`, `--web`](README.md#web) and [static](README.md#p-publish).

<a id="_187"></a>
For example, on both:<a id="_188"></a>

<a id="_189"></a>
- [https://cirosantilli.com/classification-mathematics](https://cirosantilli.com/classification-mathematics)
<a id="_190"></a>
- [https://ourbigbook.com/cirosantilli/classification-mathematics](https://ourbigbook.com/cirosantilli/classification-mathematics)
you can see a list of articles tagged by the given articles at the end of the page.

<a id="_191"></a>
Now, only on [`-W`, `--web`](README.md#web), you can also see these article lists with the article content itself, for example:<a id="_192"></a>

<a id="_193"></a>
- <a id="_194"></a>
  tagged: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

  <a id="image-ourbigbook-web-tagged-article-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/tagged.png" alt="" height="1081">

  **[Figure 19](#image-ourbigbook-web-tagged-article-list-with-body-demo). OurBigBook Web tagged article list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/tagged/classification-mathematics)

  <a id="_195"></a>
  Accessible via header links to the Tagged sections both on toplevel and non-toplevel:

  <a id="image-ourbigbook-web-toplevel-header-link-to-tagged-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/toplevel-to-tagged-arrow.png" alt="" height="736">

  **[Figure 20](#image-ourbigbook-web-toplevel-header-link-to-tagged-article-list). OurBigBook Web toplevel header link to tagged article list**. Live URL: [https://ourbigbook.com/cirosantilli/classification-mathematics](https://ourbigbook.com/cirosantilli/classification-mathematics)

  <a id="image-ourbigbook-web-non-toplevel-header-link-to-tagged-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/not-toplevel-to-tagged-arrow.png" alt="" height="783">

  **[Figure 21](#image-ourbigbook-web-non-toplevel-header-link-to-tagged-article-list). OurBigBook Web non-toplevel header link to tagged article list**. Live URL: [https://ourbigbook.com/cirosantilli/the-beauty-of-mathematics#classification-mathematics](https://ourbigbook.com/cirosantilli/the-beauty-of-mathematics#classification-mathematics)
<a id="_196"></a>
- <a id="_197"></a>
  incoming links: [https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics)

  <a id="image-ourbigbook-web-incoming-article-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/incoming.png" alt="" height="1048">

  **[Figure 22](#image-ourbigbook-web-incoming-article-list-with-body-demo). OurBigBook Web incoming article list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics](https://ourbigbook.com/go/user/cirosantilli/incoming/classification-mathematics)
<a id="_198"></a>
- <a id="_199"></a>
  children: [https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade](https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade)

  <a id="image-ourbigbook-web-incoming-child-list-with-body-demo"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/children.png" alt="" height="989">

  **[Figure 23](#image-ourbigbook-web-incoming-child-list-with-body-demo). OurBigBook Web incoming child list with body demo**. Live URL: [https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade](https://ourbigbook.com/go/user/cirosantilli/children/mammal-subclade)

  <a id="_200"></a>
  Accessible via the newly added "was limited to" info boxes when there are too many articles under a tree to show on the page:

  <a id="image-ourbigbook-web-limited-toc-size-link-to-full-child-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/limited-to-toc-arrow.png" alt="" height="620">

  **[Figure 24](#image-ourbigbook-web-limited-toc-size-link-to-full-child-article-list). OurBigBook Web limited ToC size link to full child article list**. Live URL: [https://ourbigbook.com/cirosantilli/mathematics](https://ourbigbook.com/cirosantilli/mathematics)

  <a id="image-ourbigbook-web-limited-descendant-articles-link-to-full-child-article-list"></a>
  <img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tagged-list/limited-to-articles-arrow.png" alt="" height="822">

  **[Figure 25](#image-ourbigbook-web-limited-descendant-articles-link-to-full-child-article-list). OurBigBook Web limited descendant articles link to full child article list**. Live URL: [https://ourbigbook.com/cirosantilli/mathematics](https://ourbigbook.com/cirosantilli/mathematics)

<a id="_201"></a>
The initial motivation for this was to be able to quickly browse through tagged articles, especially since the recent [tagged headers show under non-toplevel headers](#tagged-headers-show-under-non-toplevel-headers).

<a id="_202"></a>
Another motivation for this is the ability to be able to view such lists with pagination when a large number of items exists. While we don't currently limit tagged and incoming links listings, children listings are already useful as we currently limit [dynamic article tree](README.md#ourbigbook-web-dynamic-article-tree) ToCs to 1000 entries, so that children listings open up a way to explore such large article trees.

<a id="_203"></a>
This is the type of cute thing that can only be done efficiently on [`-W`, `--web`](README.md#web), where we can use an actual database to build up a precise response as requested. On [static websites](README.md#p-publish), this would either require lots of repetition on pre-rendered HTML, or making several JavaScript requests to fetch individual articles from the server, which could risk overloading the server.

<a id="_204"></a>
Announcements:<a id="_205"></a>

<a id="_206"></a>
- [https://mastodon.social/@ourbigbook/113641150832674015](https://mastodon.social/@ourbigbook/113641150832674015)
<a id="_207"></a>
- [https://x.com/OurBigBook/status/1867268408879845818](https://x.com/OurBigBook/status/1867268408879845818)
<a id="_208"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7273034333219655680/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7273034333219655680/)

## Static ToC search

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_210"></a>
It is now possible to search through ToCs on [static websites](README.md#p-publish) renders. Only items under the current ToC are searched for.

<a id="_211"></a>
Ideally we should also implement a mechanism to search across all headers from any page. This would require generating a JSON with all the headers and their renders and fetching it from JavaScript. Doable but more work. For now we keep it simple and only search the existing ToCs.

<a id="image-ourbigbook-static-search-demo-empty-search"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/static-search/empty-arrow.png" alt="" height="426">

**[Figure 26](#image-ourbigbook-static-search-demo-empty-search). OurBigBook static search demo: empty search**.

<a id="image-ourbigbook-static-search-demo-search-for-molecular-biology"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/static-search/molecular-biology-arrow.png" alt="" height="426">

**[Figure 27](#image-ourbigbook-static-search-demo-search-for-molecular-biology). OurBigBook static search demo: search for "molecular biology"**.

<a id="image-ourbigbook-static-search-demo-video"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/static-search/molecular-biology-edit.gif" alt="" height="602">

**[Figure 28](#image-ourbigbook-static-search-demo-video). OurBigBook static search demo video**.

<a id="_212"></a>
Announcements:<a id="_213"></a>

<a id="_214"></a>
- [https://x.com/OurBigBook/status/1865391481617338861](https://x.com/OurBigBook/status/1865391481617338861)
<a id="_215"></a>
- [https://mastodon.social/@ourbigbook/113611823908933805](https://mastodon.social/@ourbigbook/113611823908933805)

## Article and topic ID prefix search

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [`-W`, `--web`](README.md#web)

<a id="_217"></a>
It is now possible to search articles and topics by a given ID prefix.

<a id="_218"></a>
We are going to look full text search for non prefix searches next. But at least the frontend is working and any improvements will be backend only.

<a id="_219"></a>
Simultaneous search and sort (e.g. sorting by date and score) is also not available at present, once you start searching it disables sorting. We will also look into how to implement that.

<a id="_220"></a>
Related issue: [https://github.com/ourbigbook/ourbigbook/issues/263](https://github.com/ourbigbook/ourbigbook/issues/263)

<a id="image-ourbigbook-web-search-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/search/physics-arrow.png" alt="" height="650">

**[Figure 29](#image-ourbigbook-web-search-demo). OurBigBook Web search demo**. Visible live at: [https://ourbigbook.com/go/articles?body=false&search=physics-and](https://ourbigbook.com/go/articles?body=false&search=physics-and)

<a id="_221"></a>
Announcements:<a id="_222"></a>

<a id="_223"></a>
- [https://mastodon.social/@ourbigbook/113566032809679435](https://mastodon.social/@ourbigbook/113566032809679435)
<a id="_224"></a>
- [https://x.com/OurBigBook/status/1862460528573968858](https://x.com/OurBigBook/status/1862460528573968858)
<a id="_225"></a>
- [https://www.linkedin.com/feed/update/urn:li:activity:7268227381360787456/](https://www.linkedin.com/feed/update/urn:li:activity:7268227381360787456/)

## Tagged headers show under non-toplevel headers

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Tag](README.md#h-tag-argument)

<a id="_227"></a>
Previously, tagged articles would only show up at the bottom of the page for the toplevel header, e.g. you'd only be able to see which articles are tagged as:<a id="_228"></a>

```
Documentary film
```
under the [split header](README.md#split-headers) page:<a id="_229"></a>

```
cirosantilli.com/documentary-film
```
but not under the non-split:<a id="_230"></a>

```
cirosantilli.com/film#documentary-film
```
Now tagged articles are also shown under non-toplevel headers, both on [static websites](README.md#p-publish) and [OurBigBook Web](README.md#ourbigbook-web).

<a id="_231"></a>
This makes it much easier for readers to view the tags, as it does not require them to click the header to view it as the toplevel and then go to the bottom of the page.

<a id="_232"></a>
It also means that headers that are used primarily as tags and which would be otherwise empty now show some meaningful content.

<a id="image-non-toplevel-tagged-headers-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/tag/non-toplevel-documentary-arrows.png" alt="" height="650">

**[Figure 30](#image-non-toplevel-tagged-headers-demo). Non-toplevel tagged headers demo**. Visible live at: [https://cirosantilli.com/film#documentary-film](https://cirosantilli.com/film#documentary-film)

<a id="_233"></a>
Announcements:<a id="_234"></a>

<a id="_235"></a>
- [https://mastodon.social/@ourbigbook/113549334517651894](https://mastodon.social/@ourbigbook/113549334517651894)
<a id="_236"></a>
- [https://x.com/OurBigBook/status/1861391900948705607](https://x.com/OurBigBook/status/1861391900948705607)
<a id="_237"></a>
- [https://www.linkedin.com/feed/update/urn:li:activity:7267158458171371520](https://www.linkedin.com/feed/update/urn:li:activity:7267158458171371520)
<a id="_238"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid02xLpj976e2ciRPqNvP9kdvN7nkmrWmS18nM8hAWKtKpMKwyoCc7yr1is7UQMQsXM9l](https://www.facebook.com/OurBigBook/posts/pfbid02xLpj976e2ciRPqNvP9kdvN7nkmrWmS18nM8hAWKtKpMKwyoCc7yr1is7UQMQsXM9l)

## OurBigBook CLI enforces consistent header tree by default

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook CLI](README.md#ourbigbook-cli)

<a id="_240"></a>
[OurBigBook CLI](README.md#ourbigbook-cli) now forces you to write a consistent tree of headers by default, including e.g.:

<a id="_241"></a>
<a id="_242"></a>
- can't have text under the current header after [Includes](README.md#include). E.g. this is not allowed anymore:<a id="_243"></a>

  ```
  = Vertebrate

  Vertebrates are cool.

  \Include[mammal]

  And they have vertebrae.
  ```

  You need instead something like:<a id="_244"></a>

  ```
  = Vertebrate

  Vertebrates are cool.

  And they have vertebrae.

  \Include[mammal]
  ```
<a id="_245"></a>
- files must start with a h1 header and contain only a single h1 header. E.g. in `vertebrate.bigb` this is not allowed because it does not start with a header:<a id="_246"></a>

  ```
  I like vertebrates.

  = Vertebrate
  ```

  Neither is this because it starts with a h2 header:<a id="_247"></a>

  ```
  == Vertebrate

  I like vertebrates.
  ```

  Neither is this because it has two h1 headers:<a id="_248"></a>

  ```
  = Vertebrate

  I like vertebrates.

  = Non-vertebrate

  I don't like non vertebrates.
  ```
<a id="_249"></a>
- <a id="_250"></a>
  prevent infinite [include](README.md#include) loop recursion. E.g. this would lead to an infinite loop at render time:

  <a id="_251"></a>
  index.bigb<a id="_252"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

  <a id="_253"></a>
  vertebrate.bigb<a id="_254"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```

  <a id="_255"></a>
  mammal.bigb<a id="_256"></a>

  ```
  = Mammal

  \Include[vertebrate]
  ```

  <a id="_257"></a>
  Now you just get a nice error message instead.
<a id="_258"></a>
- <a id="_259"></a>
  every file must be recursively included from [the toplevel index file](README.md#the-toplevel-index-file). E.g.

  <a id="_260"></a>
  index.bigb<a id="_261"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

  <a id="_262"></a>
  vertebrate.bigb<a id="_263"></a>

  ```
  = Vertebrate
  ```

  <a id="_264"></a>
  mammal.bigb<a id="_265"></a>

  ```
  = Mammal
  ```

  <a id="_266"></a>
  would give an error because `mammal.bigb` is not included from anywhere. To fix it you would likely want:

  <a id="_267"></a>
  vertebrate.bigb<a id="_268"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```
<a id="_269"></a>
- <a id="_270"></a>
  files cannot be included twice. Previously the following was allowed:

  <a id="_271"></a>
  index.bigb<a id="_272"></a>

  ```
  = My homepage

  \Include[vertebrate]
  \Include[mammal]
  ```

  <a id="_273"></a>
  vertebrate.bigb<a id="_274"></a>

  ```
  = Vertebrate

  \Include[mammal]
  ```

  <a id="_275"></a>
  mammal.bigb<a id="_276"></a>

  ```
  = Mammal
  ```

  <a id="_277"></a>
  But now it gives an error because `mammal.bigb` is included from both `index.bigb` and `vertebrate.bigb`.

  <a id="_278"></a>
  To fix it you would likely instead want to include it only from the most specific location `vertebrate.bigb` and remove it from `index.bigb`:

  <a id="_279"></a>
  index.bigb<a id="_280"></a>

  ```
  = My homepage

  \Include[vertebrate]
  ```

<a id="_281"></a>
It is a common issue with most plaintext note taking systems that they don't force you to make a consistent tree.

<a id="_282"></a>
However, for publishing, having one tree is essential, otherwise it can be very hard for users to navigate your content.

<a id="_283"></a>
Furthermore, this makes things much simpler to implement and understand for OurBigBook Web and a future WYSIWYG local editor.

<a id="_284"></a>
Some other pedantry:

<a id="_285"></a>
<a id="_286"></a>
- rename `README.bigb` to `index.bigb` for the [the toplevel index file](README.md#the-toplevel-index-file). Much cleaner, and we already have a conflict on the baseneme index with index.html, so why create another conflict with README
<a id="_287"></a>
- rename [the `_out` directory](README.md#the-out-directory) from `out` to `_out`, which is a reserved ID. Otherwise it was impossible to have a directory called `out` with ourbigbook files for [directory-based `scope`](README.md#directory-based-scope).

<a id="_288"></a>
While [OurBigBook Web](README.md#ourbigbook-web) topic mind melding remains the most innovative feature of the project, local plaintext is a fundamental guarantee that you will never lose your content, and we intend to keep it awesome.

<a id="_289"></a>
Announcements:<a id="_290"></a>

<a id="_291"></a>
- [https://mastodon.social/@ourbigbook/113549071062984064](https://mastodon.social/@ourbigbook/113549071062984064)
<a id="_292"></a>
- [https://x.com/OurBigBook/status/1861383431973683551](https://x.com/OurBigBook/status/1861383431973683551)

<h2 id="ourbigbook-com-cirosantilli-loads-2x-as-fast-after-database-optimizations">ourbigbook.com/cirosantilli loads 2x as fast after database optimizations</h2>

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web performance benchmarking](README.md#ourbigbook-web-performance-benchmarking), [`-W`, `--web`](README.md#web)

<a id="_295"></a>
At [https://github.com/ourbigbook/ourbigbook/commit/075872a0a5ca7faf171d45834bc2b47995a15634](https://github.com/ourbigbook/ourbigbook/commit/075872a0a5ca7faf171d45834bc2b47995a15634) and nearby previous commits we've optimized the database queries made on article pages, mostly by adding some key missing indices and cache columns.

<a id="_296"></a>
As a result, [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli) now starts downloading the first byte 2x as fast as before, going down from about 1200 ms to around 600 ms, at a time region which makes a huge difference for user experience.

<a id="_297"></a>
We will also start keeping better performance logs at: [Section "OurBigBook Web performance log"](README.md#ourbigbook-web-performance-log) to make sure we don't regress as easily.

<a id="_298"></a>
Announcements:<a id="_299"></a>

<a id="_300"></a>
- [https://mastodon.social/@ourbigbook/113068626468247721](https://mastodon.social/@ourbigbook/113068626468247721)
<a id="_301"></a>
- [https://x.com/OurBigBook/status/1830626456235299211](https://x.com/OurBigBook/status/1830626456235299211)
<a id="_302"></a>
- [https://www.linkedin.com/feed/update/urn:li:share:7236392360090243075](https://www.linkedin.com/feed/update/urn:li:share:7236392360090243075)
<a id="_303"></a>
- [https://www.facebook.com/OurBigBook/posts/pfbid029F6xK7QrV725cAfFoVbb2RhGtKXvfzqBDcy2kvY1AALNSHDbnbuvZJkYFhzmejUcl](https://www.facebook.com/OurBigBook/posts/pfbid029F6xK7QrV725cAfFoVbb2RhGtKXvfzqBDcy2kvY1AALNSHDbnbuvZJkYFhzmejUcl)

## Visual Studio Code extension overhaul

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Visual Studio Code](README.md#visual-studio-code)

<a id="_305"></a>
We've greatly improved the [Visual Studio Code extension](README.md#visual-studio-code) adding support for the most important VS Code language features: Ctrl + T header search, Ctrl + click jump to header, header outline and link autocomplete

<a id="_306"></a>
Thanks to [Juhani Junkala](https://x.com/subspace_audio) for the awesome CC0 chiptune game soundtrack! [https://opengameart.org/content/5-chiptunes-action](https://opengameart.org/content/5-chiptunes-action)

<a id="video-ourbigbook-visual-studio-code-extension"></a>
**[Video 1](#video-ourbigbook-visual-studio-code-extension). OurBigBook Visual Studio Code extension.** [Source](https://www.youtube.com/watch?v=0W8U2YtQ8fg).

<a id="_307"></a>
Announcements:<a id="_308"></a>

<a id="_309"></a>
- [https://mastodon.social/@ourbigbook/112926933386595349](https://mastodon.social/@ourbigbook/112926933386595349)
<a id="_310"></a>
- [https://x.com/OurBigBook/status/1821559960687305015](https://x.com/OurBigBook/status/1821559960687305015)
<a id="_311"></a>
- [https://www.youtube.com/watch?v=0W8U2YtQ8fg](https://www.youtube.com/watch?v=0W8U2YtQ8fg)
<a id="_312"></a>
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7227327143402184704/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7227327143402184704/)
<a id="_313"></a>
- [https://www.facebook.com/reel/1023654756429291](https://www.facebook.com/reel/1023654756429291)

## Body preview on all article lists

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web](README.md#ourbigbook-web)

<a id="_315"></a>
The article body now shows by default on all article lists. So do comment lists.

<a id="_316"></a>
The major application of this is to quickly browser through a users's top or latest posts, e.g. [https://ourbigbook.com/go/user/cirosantilli/articles?sort=score](https://ourbigbook.com/go/user/cirosantilli/articles?sort=score)

<a id="_317"></a>
Previously, the body would only show on:<a id="_318"></a>

<a id="_319"></a>
- [topic](README.md#ourbigbook-web-topics) listings
<a id="_320"></a>
- discussion comment lists

<a id="_321"></a>
Now it shows everywhere else as well, except that in other views, only a fixed height preview is shown to allow quickly going through large articles without too much scrolling.

<a id="_322"></a>
A "view more" button can uncover the hidden content if the user wishes to usee it.

<a id="_323"></a>
A "Show body" control was also added to toggle body vs the previously existing table mode.

<a id="video-view-more-and-show-body-demo"></a>
**[Video 2](#video-view-more-and-show-body-demo). View more and show body demo.** [Source](https://www.youtube.com/watch?v=4Pxphm7N6_0).

<a id="image-view-more-and-show-body-demo"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/view-more/demo.png" alt="" height="2000">

**[Figure 31](#image-view-more-and-show-body-demo). View more and show body demo**.

<a id="_324"></a>
Announcements:<a id="_325"></a>

<a id="_326"></a>
- [https://mastodon.social/@ourbigbook/112791709657088236](https://mastodon.social/@ourbigbook/112791709657088236)
<a id="_327"></a>
- [https://x.com/OurBigBook/status/1812905677817340219](https://x.com/OurBigBook/status/1812905677817340219)

## Unlisted articles on web

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web](README.md#ourbigbook-web)

<a id="_329"></a>
It is now possible to mark articles as unlisted on [OurBigBook Web](README.md#ourbigbook-web): [Section "OurBigBook Web unlisted content"](README.md#ourbigbook-web-unlisted-articles).

<a id="_330"></a>
The most important effect of this is that unlisted articles don't show on the table of contents of its ancestors. They also don't show on many article listing by default, e.g. on the list of user's latest articles.

<a id="_331"></a>
The main use case we have for this feature right now is to stop polluting the table of contents with articles a user does not wish to show, and especially when doing [local to Web upload](README.md#web), where Web articles are marked as unlisted by default if they are deleted locally.

<a id="_332"></a>
We offer unlisted as an alternative to deletion for now because of the general philosophy what "permalinks should never break". This is currently not true as we don't have article history and therefore no permalinks. However, once history is implemented, we want to make it so links to specific versions will never ever break by forbidding article and history deletion entirely. Marking articles as unlisted will then allows to prevent deletion, while still keeping table of contents tidy.

<a id="_333"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/unlisted-articles/article-page.png" alt="" height="612">

**[Figure 32](#_333)** The unlisted status is shown as a pill on the article metadata.

<a id="_334"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/unlisted-articles/topic.png" alt="" height="276">

**[Figure 33](#_334)** Unlisted articles don't show by default on the topics page, but it is possible to show them by clicking the link at the bottom of the page.

<a id="_335"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/unlisted-articles/topic-show.png" alt="" height="621">

**[Figure 34](#_335)** After that, unlisted articles are also shown.

<a id="_336"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/unlisted-articles/editor.png" alt="" height="425">

**[Figure 35](#_336)** A new metadata tab was added to the [web editor](README.md#web-editor).

<a id="_337"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/unlisted-articles/editor-metadata.png" alt="" height="398">

**[Figure 36](#_337)** The unlisted status can be seen and edited from the newly added metadata tab of the web editor.

## A few articles in same topic are shown at the bottom of every article page

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web](README.md#ourbigbook-web), [Topic](README.md#ourbigbook-web-topics)

<a id="_340"></a>
In order to give more immediate [topic](README.md#ourbigbook-web-topics) value to readers, and to better highlight the [topics](README.md#ourbigbook-web-topics) feature, we now show a few articles on the same topic at the bottom of every article page, essentially acting as a preview of the corresponding topic page.

<a id="_341"></a>
For example, if you visit the "Calculus" article by user Barack Obama: [https://ourbigbook.com/barack-obama/calculus](https://ourbigbook.com/barack-obama/calculus) then at the bottom of the page you can see a section "Articles by others on the same topic (3)" which displays up to the 5 most highly upvoted articles in the same topic written by other users, much like the topic page for the "Calculus" topic: [https://ourbigbook.com/go/topic/calculus](https://ourbigbook.com/go/topic/calculus).

<a id="_342"></a>
By comparison, the topic page shows more articles by default (20), supports pagination, and allows for other forms of sorting such as viewing the latest articles in a topic. We are initially not adding those options to the article page itself as there is already enough stuff going on there.

<a id="_343"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/topics-on-every-article-page.png" alt="" height="1532">

<a id="_344"></a>
Announcements:<a id="_345"></a>

<a id="_346"></a>
- [https://mastodon.social/@ourbigbook/112557950474730532](https://mastodon.social/@ourbigbook/112557950474730532)
<a id="_347"></a>
- [https://x.com/OurBigBook/status/1797943367420326011](https://x.com/OurBigBook/status/1797943367420326011)

## Short URL fragments on OurBigBook Web

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Dynamic article tree](README.md#ourbigbook-web-dynamic-article-tree), [Implemented by sidstuff](README.md#implemented-by-sidstuff), [OurBigBook Web](README.md#ourbigbook-web)

<a id="_351"></a>
Previously, when clicking a link to an element that is present in the current page, the URL fragment would contain the full ID that element.

<a id="_352"></a>
Now, only the ID relative to URL path shows.

<a id="_353"></a>
A very common use case for this is when clicking table of content items.

<a id="_354"></a>
For exmple, from [https://ourbigbook.com/barack-obama/mathematics](https://ourbigbook.com/barack-obama/mathematics), clicking the ToC item for "Calculus" would previously lead to [https://ourbigbook.com/barack-obama/mathematics#barack-obama/calculus](https://ourbigbook.com/barack-obama/mathematics#barack-obama/calculus)

<a id="_355"></a>
After this change it leads just to: [https://ourbigbook.com/barack-obama/mathematics#calculus](https://ourbigbook.com/barack-obama/mathematics#calculus), without repeating the "`#barack-obama` part as it already appears in the URL path `/barack-obama/mathematics`.

<a id="_356"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/short-fragment.png" alt="" height="800">

<a id="_357"></a>
Short URLs were already used on [Static website](README.md#p-publish) publishes, and weren't implemented on [OurBigBook Web](README.md#ourbigbook-web) yet simply because this is hard. The reason this was much harder to implement on Web is that due to [Dynamic article trees](README.md#ourbigbook-web-dynamic-article-tree) we can't know at render-time what the correct fragment will be, as it depends on what shows on the page or not.

<a id="_358"></a>
And furthermore, articles by different users can appear on the same page due to [topics](README.md#ourbigbook-web-topics).

<a id="_359"></a>
The simple but not ideal solution that we were using up to now was to just have full IDs on every HTML element, make every a point to an absolute ID like `/barack-obama/mathematics`, and then use JS effect to hack that to `#barack-obama/mathematics` if the element is in the page.

<a id="_360"></a>
What we did now is to take the Js hacks one step further, and actually replace the "long URLs" with short ones. This was not easy, partly because the browser interfaces are not amazing in that area, partly due to fighting with React. But we manage to get it working mostly well.

<a id="_361"></a>
Announcements:<a id="_362"></a>

<a id="_363"></a>
- [https://mastodon.social/@ourbigbook/112553597134131989](https://mastodon.social/@ourbigbook/112553597134131989)
<a id="_364"></a>
- [https://x.com/OurBigBook/status/1797665231273177182](https://x.com/OurBigBook/status/1797665231273177182)

## `\Hr` horizontal rule macro created

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Horizontal rule](README.md#horizontal-rule), [Implemented by sidstuff](README.md#implemented-by-sidstuff)

<a id="_367"></a>
Docs: [Section "Horizontal rule"](README.md#horizontal-rule)

<a id="_368"></a>
Behold:<a id="_369"></a>

```
Before the rule.

More before the rule.

\Hr

After the rule.

More after the rule.
```
<a id="_370"></a>
which renders as:

<a id="_371"></a>


> <a id="_372"></a>
> Before the rule.
> 
> <a id="_373"></a>
> More before the rule.
> 
> <a id="_374"></a>
> ---
> 
> <a id="_375"></a>
> After the rule.
> 
> <a id="_376"></a>
> More after the rule.

## Gray on gray color replaces green on black and many other CSS improvements

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Implemented by sidstuff](README.md#implemented-by-sidstuff)

<a id="_378"></a>
We're experimenting with a more traditional and boring "dark" theme than the green on black classic previously used.

<a id="_379"></a>
Readability is probably slightly better, though it is hard to measure these things. It is quite possible that the change matter much more for some people than others who have different eye sight phenotypes.

<a id="_380"></a>
Perhaps the most important outcome of this is that it will greatly reduce the endless complaining from the community. Though perhaps that was a feature rather than a bug?

<a id="_381"></a>
Beyond the theme change, many other changes were made. Many of those improvements feel like undisputable upgrades, e.g.:<a id="_382"></a>

<a id="_383"></a>
- headers are not colored differently from regular text
<a id="_384"></a>
- table borders are less visible
<a id="_385"></a>
- navbar and footer are more discrete and readable

<a id="_386"></a>
The CSS code was also refactored and it is not much easier to make broad color changes such as these in the future, as color constants are not more closely grouped, and fewer constants are now used.

<a id="_387"></a>
Large parts of this change were pushed forward by [sidstuff](README.md#sidstuff) who contributed a several code snippets and ideas to it.

<a id="_388"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/article-list-gray.png" alt="" height="450">

<a id="_389"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/article-list-green.png" alt="" height="450">

<a id="_390"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/footer-gray.png" alt="" height="450">

<a id="_391"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/footer-green.png" alt="" height="450">

<a id="_392"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/donald-trump-algebra-gray.png" alt="" height="850">

<a id="_393"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/gray-on-gray/donald-trump-algebra-green.png" alt="" height="850">

## Intro to OurBigBook video

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Publicity](README.md#publicity)

<a id="video-intro-to-the-ourbigbook-project"></a>
**[Video 3](#video-intro-to-the-ourbigbook-project). Intro to the OurBigBook Project.** [Source](https://www.youtube.com/watch?v=BR2dXeR5jt8).

## Pinned article

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web](README.md#ourbigbook-web)

<a id="_396"></a>
It is now possible for admins pin an article to the homepage. The initial use case is to help with new user onboarding. Documentation: [pinned article](#pinned-article).

<a id="_397"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/pinned-article/pinned-article-on-topics-page-arrow.png" alt="" height="1200">

<h2 id="automatically-create-file-pages-for-every-file">Automatically create <code>_file</code> pages for every file</h2>

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Static website](README.md#p-publish)

<a id="_399"></a>
Previously we would only create an entry in the [`_file` output directory](README.md#file-output-directory) for [headers](README.md#header) marked wiht the [`\H` `file` argument](README.md#h-file-argument).

<a id="_400"></a>
For example the file [file_demo/hello_world.js](file_demo/hello_world.js) in this repository has an associated header with the `file` argument in our [index.bigb](index.bigb) :<a id="_401"></a>

```
= file_demo/hello_world.js
{file}

An explanation of what this text file is about.

Another line.
```

<a id="_402"></a>
As a result, when doing a [split header](README.md#split-headers) conversion, it would get both:<a id="_403"></a>

<a id="_404"></a>
- a [`_file` output directory](README.md#file-output-directory) page at path `_file/file_demo/hello_world.js` [file\_demo/hello\_world.js](README.md#_file/file_demo/hello_world.js)
<a id="_405"></a>
- a [`_raw` directory](README.md#raw-directory) page at path `_raw/file_demo/hello_world.js` [file_demo/hello_world.js](file_demo/hello_world.js)

<a id="_406"></a>
On the other hand, the test file [file_demo/nofile.js](file_demo/nofile.js) has no such associated header in the source code.

<a id="_407"></a>
Before this change, [file_demo/nofile.js](file_demo/nofile.js) would only get an [`_raw` directory](README.md#raw-directory) entry under `_raw/file_demo/nofile.js` and not `_file` entry. But now it also gets both.

<a id="_408"></a>
The advantages of a `_file` entries over `_raw` entries are as follows:<a id="_409"></a>

<a id="_410"></a>
- `_file` entries can have metadata such as:<a id="_411"></a>

  <a id="_412"></a>
  - OurBigBook content associated to them when they have an associated `_file` header. For example at [file\_demo/hello\_world.js](README.md#_file/file_demo/hello_world.js) we can see the rendered text:<a id="_413"></a>
    > <a id="_414"></a>
    > An explanation of what this text file is about.
    > 
    > <a id="_415"></a>
    > Another line.

    Of course, in that case, they would also get the `_file` entry even before this update. However, this update does allow for a smooth update path where you can first link to the `_file` entry from external websites, and then add comments as needed later on without changing URLs.
  <a id="_416"></a>
  - Google Analytics and other features via [ourbigbook.liquid.html](README.md#ourbigbook-liquid-html)
<a id="_417"></a>
- `_file` always shows on static website hosts like GitHub Pages, since they are just HTML pages. This is unlike `raw` files which may just get downloaded for unknown extensions like `.bigb` rather than displayed on the browser: [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](README.md#raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages)

<a id="_418"></a>
This change is especially powerful following [Always show large text files on `_file` split headers](#always-show-large-text-files-on-file-split-headers).

<a id="_419"></a>
Because we now have `_file` entries for every single file, we have also modified [`_dir` directory](README.md#dir-directory) directory listing pages to link to `_file` entries as those are generally more useful than `_raw` which is what they previously linked to. And you can always reach `_reaw_` from the corresponding `_file` is needed. Example: [https://docs.ourbigbook.com/_dir](https://docs.ourbigbook.com/_dir)

<h2 id="always-show-large-text-files-on-file-split-headers">Always show large text files on <code>_file</code> split headers</h2>

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [Static website](README.md#p-publish)

<a id="_421"></a>
Previously, large files with an [`\H` `file` argument](README.md#h-file-argument) associated to them would show a message<a id="_422"></a>

```
index.js was not rendered because it is too large (> 2000 bytes)
```
rather than the file contents both on their split and non-split versions, e.g.:<a id="_423"></a>

<a id="_424"></a>
- [https://docs.ourbigbook.com/#_file/index.js](https://docs.ourbigbook.com/#_file/index.js)
<a id="_425"></a>
- [https://docs.ourbigbook.com/_file/index.js](https://docs.ourbigbook.com/_file/index.js)

<a id="_426"></a>
Now, the split version [https://docs.ourbigbook.com/_file/index.js](https://docs.ourbigbook.com/_file/index.js) alwayws shows the full text file.

<a id="_427"></a>
When not in split mode, limiting preview sizes is important otherwise multi-header pages might become far too big. Ideally we would have found a way to reliably use `iframe` + `loading="lazy"` to refer to the file without actually embedding it into the page as we do for images, but we haven't managed to do that so far.

<a id="_428"></a>
This allows us to now see files that were previously not visible anywhere on the rendered HTML without download due to [`_raw` files are downloaded rather than displayed in browser for certain file extensions on GitHub Pages](README.md#raw-files-are-downloaded-rather-than-displayed-in-browser-for-certain-file-extensions-on-github-pages).

<a id="_429"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/always-show-large-files-on-split-headers.png" alt="" height="700">

## Optimize generated HTML size by adding on-the-fly elements

↑ **Parent:** [News](news.md)

<a id="_430"></a>
The main focus was the [Table of contents](README.md#table-of-contents) rendering, which had a lot of redundant stuff. Headers were the next largest gain.

<a id="_431"></a>
The main techniques used to reduce size were:<a id="_432"></a>

<a id="_433"></a>
- auto-generate a few elements on-the-fly with JavaScript for on-hover effects, but only if it doesn't affect SEO and readability when JS is turned off
<a id="_434"></a>
- use a lot more CSS `::after` and `::before` to avoid embedding repetitive icons multiple times on the HTML

<a id="_435"></a>
After this changes, the rendered size of cirosantilli.com fell from 216 MiB to 156.5 MiB, which is kind of cool!

<h2 id="suggest-article-creation-for-topics-that-don-t-exist">Suggest article creation for topics that don't exist</h2>

↑ **Parent:** [News](news.md)  
🏷️ **Tags:** [OurBigBook Web](README.md#ourbigbook-web)

<a id="_437"></a>
In previous updates we added [shorthand topic links](README.md#shorthand-topic-link) which allow you to write `#mathematics` to link to [OurBigBook Web topics](README.md#ourbigbook-web-topics) such as: [https://ourbigbook.com/go/topic/mathematics](https://ourbigbook.com/go/topic/mathematics)

<a id="_438"></a>
The outcome of that however is that it is also easy and correct to create links to topics that don't yet exist on the [OurBigBook Web](README.md#ourbigbook-web) instance.

<a id="_439"></a>
To make this nicer, we've unconsciously copied Wikipedia once again, and added a "Create an article for this topic" link

<a id="_440"></a>
For example, currently [OurBigBook.com](README.md#ourbigbook-com) the topic "Endoplasmatic Reticulum" does not have any articles on it. So if you created a link `<#endoplasmatic reticulum>`, it would redirect you to: [https://ourbigbook.com/go/topic/endoplasmic-reticulum](https://ourbigbook.com/go/topic/endoplasmic-reticulum)

<a id="_441"></a>
Previously, this would show "Topic does not exist". But now it shows a button that opens the new article editor with pre-filled title "Endoplasmatic reticulum". The title choice is only a heuristic as it can't know the correct capitalization, but it covers most cases corectly by default and can be modified manually as needed.

<a id="_442"></a>
![](https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/suggest-new-article-for-empty-topic/topic-page-arrow.png)

<a id="_443"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/suggest-new-article-for-empty-topic/new-article-page.png" alt="" height="700">

## ↑ Ancestors (3)

1. [Publicity](README.md#publicity)
2. [Developing OurBigBook](README.md#developing-ourbigbook)
3. [OurBigBook Project](README.md)

## ← Incoming links (1)

- [OurBigBook Project](README.md)
