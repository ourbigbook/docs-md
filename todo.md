# TODO

↑ **Parent:** [OurBigBook Project](README.md)

**Table of contents**

- [Issues](#issues)
  - [Encrypted client hello](#encrypted-client-hello)
  - [Add button on web to move article to trash on web](#add-button-on-web-to-move-article-to-trash-on-web)
  - [Convert ordered list Ol to a boolean argument of unordered lists Ul](#convert-ordered-list-ol-to-a-boolean-argument-of-unordered-lists-ul)
  - [Allow linking to auto-generated files](#allow-linking-to-auto-generated-files)
  - [Link to \_file rather than \_raw if there's split pages](#link-to-file-rather-than-raw-if-there-s-split-pages)
  - [Show directory listings on `{file}` headers](#show-directory-listings-on-file-headers)
  - [Nested set index corruption](#5)
  - [Like and unlike requests are very slow](#like-and-unlike-requests-are-very-slow)
  - [Incoming links and tagged metadata does not show synonyms](#incoming-links-and-tagged-metadata-does-not-show-synonyms)
  - [Image title with x to image with content incorrectly disallowed](#image-title-with-x-to-image-with-content-incorrectly-disallowed)
  - [Lint tables for correct number of columns](#lint-tables-for-correct-number-of-columns)
  - [Remove synonym from JSON, use Ref.type = synonym instead](#remove-synonym-from-json-use-ref-type-synonym-instead)
  - [Forbid uppercase IDs on web and CLI by default](#forbid-uppercase-ids-on-web-and-cli-by-default)
  - [Option to add view on ourbigbook link on header metadata of CLI static renders](#option-to-add-view-on-ourbigbook-link-on-header-metadata-of-cli-static-renders)
  - [Reorder convert to move Article.destroySideEffect before File.destroy](#4)
  - [List synonyms on metadata section](#list-synonyms-on-metadata-section)
  - [Move all header metadata from source to HTML in Web](#web-header-metadata-to-widgets)
  - [Fix parentId and previousSiblingId on articles API](#fix-parentid-and-previoussiblingid-on-articles-api)
  - [Id, Ref and File foreign normalization](#ref-file-normalization)
  - [Allow creation of multiple headers in one go on web](#web-create-multiple-headers)
  - [Option to add zip of local conversion to converted GitHub pages website](#option-to-add-zip-of-local-conversion-to-converted-github-pages-website)
  - [Cross source file word count is always 0 on ToC hover](#3)
  - [Internal cross reference to non-existent ID is not checked before render the second time we try to convert](#1)
  - [Add a `File:` prefix to `{file}` headers](#add-a-file-prefix-to-file-headers)
  - [Allow `{parent}` to point to `{file}` header](#allow-parent-to-point-to-file-header)
  - [Show likers list on article page](#show-likers-list-on-article-page)
  - [Show like and follow date on user like follow lists](#show-like-and-follow-date-on-user-like-follow-lists)
  - [Handle email replies to notification@ourbigbook.com](#handle-email-replies-to-notification-at-ourbigbook-com)
  - [Firefox tab lists don't wrap](#firefox-tab-lists-don-t-wrap)
  - [Follow topic](#follow-topic)
  - [At mention and topics on web](#at-mention-and-topics-on-web)
  - [At mention and topics locally](#at-mention-and-topics-locally)
  - [View article and issue likers and followers](#view-article-and-issue-likers-and-followers)
  - [Like comments](#like-comments)
  - [Use same parent title if the current user has a matching article when clicking "Create my own version of article" ](#use-same-parent-title-if-the-current-user-has-a-matching-article-when-clicking-create-my-own-version-of-article)
  - [Delete article](#delete-article)
  - [Serialize parsed build-in KaTeX macros](#serialize-parsed-build-in-katex-macros)
  - [Handle web upload after local article renaming with synonym redirection set](#handle-web-upload-after-local-article-renaming-with-synonym-redirection-set)
  - [Photos of the merchandise!](#photos-of-the-merchandise)
  - [Flyers](#flyers)
  - [ourbigbook.com --web uploads sometimes fail with ETIMEDOUT or ECONNRESET](#ourbigbook-com-web-uploads-sometimes-fail-with-etimedout-or-econnreset)
  - [Header followed by paragraph without blank line does not split correctly](#header-followed-by-paragraph-without-blank-line-does-not-split-correctly)
  - [Store SHA of each article + descendants and skip API re-renders for entire subtrees](#store-sha-of-each-article-plus-descendants-and-skip-api-re-renders-for-entire-subtrees)
  - [Multiheader editing](#multiheader-editing)
  - [Make open and close arrows have the same height on ToC](#make-open-and-close-arrows-have-the-same-height-on-toc)
  - [Add sibling/add child buttons next to toc entries of articles owned by the current user](#add-sibling-add-child-buttons-next-to-toc-entries-of-articles-owned-by-the-current-user)
  - [Progress spinner after submit](#progress-spinner-after-submit)
  - [Hide unconfirmed users](#hide-unconfirmed-users)
  - [Fragment redirects not working on web](#fragment-redirects-not-working-on-web)
  - [WYSIWYG](#wysiwyg)
  - [Live error checking as you type on editor if chosen previous sibling is not a child of the selected parent article](#live-error-checking-as-you-type-on-editor-if-chosen-previous-sibling-is-not-a-child-of-the-selected-parent-article)
  - [Reach the same performance as static website with dynamic tree](#reach-the-same-performance-as-static-website-with-dynamic-tree)
  - [Inject React header metadata on each header separately](#inject-react-header-metadata-on-each-header-separately)
  - [Include should work transparently with README in subdirectory](#include-should-work-transparently-with-readme-in-subdirectory)
  - [Remove the path parameter from the article creation API](#remove-the-path-parameter-from-the-article-creation-api)
  - [Statically render links to issues and topic under each header for better SEO](#statically-render-links-to-issues-and-topic-under-each-header-for-better-seo)
- [Make rendered issue and comment fragments as short as possible](#make-rendered-issue-and-comment-fragments-as-short-as-possible)
- [Cannot link from comment to article](#cannot-link-from-comment-to-article)
  - [Clicking on the comment header does not highlight the header line](#clicking-on-the-comment-header-does-not-highlight-the-header-line)
  - [Comment h1 self link is empty and thus refreshes the page](#comment-h1-self-link-is-empty-and-thus-refreshes-the-page)
  - [Remove all unnecessary newlines from HTML output](#remove-all-unnecessary-newlines-from-html-output)
  - [ToC link on headers not opening collapsed toc entries](#toc-link-on-headers-not-opening-collapsed-toc-entries)
  - [parentId dropdown autocomplete](#parentid-dropdown-autocomplete)
  - [LIKE metadata on JOIN on](#like-metadata-on-join-on)
  - [Load more articles](#load-more-articles)
  - [Load more ToC entrie](#load-more-toc-entrie)
  - [Word count on web](#word-count-on-web)
  - [Monaco editor requires web](#monaco-editor-requires-web)
  - [Respect ourbigbook.json `htmlXExtension` on ourbigbook.json redirects](#respect-ourbigbook-json-htmlxextension-on-ourbigbook-json-redirects)
  - [iframe macro](#iframe-macro)
- [Closed issues](#closed-issues)
  - [Allow disambiguate and id header arguments on web](#allow-disambiguate-and-id-header-arguments-on-web)
  - [Remove scope from toc entry IDs](#remove-scope-from-toc-entry-ids)
  - [split and nosplit links missing from cirosantilli.com](#split-and-nosplit-links-missing-from-cirosantilli-com)
  - [Move articles deleted locally to under a trash article on web](#move-articles-deleted-locally-to-under-a-trash-article-on-web)
  - [Vs Code symbol provider](#vs-code-symbol-provider)
  - [Allow creating new pages under scope on web](#allow-creating-new-pages-under-scope-on-web)
  - [Show tagged list of non toplevel pages](#show-tagged-list-of-non-toplevel-pages)
  - [Shorthand block quotes](#shorthand-block-quotes)
  - [ToC Js folding broken on Web](#toc-js-folding-broken-on-web)
  - [Allow user to edit other user's articles](#allow-user-to-edit-other-user-s-articles)
  - [Blowup with unclosed image followed by math](#blowup-with-unclosed-image-followed-by-math)
  - [Ordered list lost when rendering to bigb output format](#ordered-list-lost-when-rendering-to-bigb-output-format)
  - [Render large files on split headers](#render-large-files-on-split-headers)
  - [Don't use helper synthetic AST nodes, render at render time instead](#remove-synthetic-asts)
  - [View article source on web](#view-article-source-on-web)
  - [Benchmark and optimize output size](#benchmark-and-optimize-output-size)
  - [Web upload fails when renaming a header to a synonym](#web-upload-fails-when-renaming-a-header-to-a-synonym)
  - [Render ancestors, incoming links and tagged on web](#render-ancestors-incoming-links-and-tagged-on-web)
  - [Vertical scrollbar when image title contains math underscore](#vertical-scrollbar-when-image-title-contains-math-underscore)
  - [Make articles removed locally empty on web upload](#make-articles-removed-locally-empty-on-web-upload)
  - [Don't skip parent/previous sibling updates on --web uploads](#don-t-skip-parent-previous-sibling-updates-on-web-uploads)
  - [CLI nosplit points to self](#cli-nosplit-points-to-self)
  - [Pass previousSiblingId on web upload](#pass-previoussiblingid-on-web-upload)
  - [Links to synonym header have fragment](#links-to-synonym-header-have-fragment)
  - [Put raw files in a separate magic prefix](#put-raw-files-in-a-separate-magic-prefix)
  - [Synonym redirects on web](#synonym-redirects-on-web)
  - [Start a basic notification system](#start-a-basic-notification-system)
  - [Find a way to show index.html raw files that get overriden by directory listings](#2)
  - [Automatically add `source` to archive.org images](#automatically-add-source-to-archive-org-images)
  - [Put files in a separate namespace](#put-files-in-a-separate-namespace)
  - [Following and followed tabs are swapped](#following-and-followed-tabs-are-swapped)
  - [Undefined tag error message for directory conversion says header ID is not defined instead of tag ID](#undefined-tag-error-message-for-directory-conversion-says-header-id-is-not-defined-instead-of-tag-id)
  - [Design a project banner](#design-a-project-banner)
  - [Subsections missing on web dynamic tree](#subsections-missing-on-web-dynamic-tree)
  - [Enable web math defines default on non-web](#enable-web-math-defines-default-on-non-web)
  - [Enable web math defines on web editor](#enable-web-math-defines-on-web-editor)
  - [Store auto-formated bigb source on web](#store-auto-formated-bigb-source-on-web)
  - [Split \_out/bigb and \_out/web](#split-out-bigb-and-out-web)
  - [Skip re-render from API if article was unchanged](#skip-re-render-from-api-if-article-was-unchanged)
  - [Computer sticker](#computer-sticker)
  - [Prevent full page reload on links using our existing link capture](#prevent-full-page-reload-on-links-using-our-existing-link-capture)
  - [Second meta line showing up on index page even if empty](#second-meta-line-showing-up-on-index-page-even-if-empty)
  - [Article create and update slow on web](#article-create-and-update-slow-on-web)
    - [Article create and update slow on web update 1](#article-create-and-update-slow-on-web-update-1)
  - [Donate button on web](#donate-button-on-web)
  - [`(beta)` on navbar gets pushed down half way at a specific page width just above mobile shift](#beta-on-navbar-gets-pushed-down-half-way-at-a-specific-page-width-just-above-mobile-shift)
  - [Empty Latest Followed shows as There are no articles on this website yet](#empty-latest-followed-shows-as-there-are-no-articles-on-this-website-yet)
  - [Add sibling/add child buttons next to headers owned by the current user](#add-sibling-add-child-buttons-next-to-headers-owned-by-the-current-user)
  - [Infinite navbar profile image refresh loop when there is no Internet](#infinite-navbar-profile-image-refresh-loop-when-there-is-no-internet)
  - [Separate lines with field label for parent and previous sibling on web editor](#separate-lines-with-field-label-for-parent-and-previous-sibling-on-web-editor)
  - [Allow showing article body on article lists](#allow-showing-article-body-on-article-lists)
  - [Comment h1 has empty metadata line where likes would be placed](#comment-h1-has-empty-metadata-line-where-likes-would-be-placed)
  - [Comment autogenerated IDs are wrong when there is header in the comment](#comment-autogenerated-ids-are-wrong-when-there-is-header-in-the-comment)
  - [Add an option to add a prefix to every ID of rendered output to avoid conflicts across comments and issue](#add-an-option-to-add-a-prefix-to-every-id-of-rendered-output-to-avoid-conflicts-across-comments-and-issue)
  - [First on-hover heder self link after table of content activates table of contents instead of header ](#first-on-hover-heder-self-link-after-table-of-content-activates-table-of-contents-instead-of-header)
  - [h2 on hover self links are empty on Web](#h2-on-hover-self-links-are-empty-on-web)
  - [Test scope 2 appears after Test scope 1 on generated data](#test-scope-2-appears-after-test-scope-1-on-generated-data)
  - [Prefix unnumbered IDs with the parent header's ID](#prefix-unnumbered-ids-with-the-parent-header-s-id)
  - [Remove @ from toc IDs](#remove-at-from-toc-ids)
  - [Missing header metadata such as like button, same topic and issue link on headers under a scope](#missing-header-metadata-such-as-like-button-same-topic-and-issue-link-on-headers-under-a-scope)
  - [Headers under scope don't have scope on ID leads to ID conflicts and a link misses on Web](#headers-under-scope-don-t-have-scope-on-id-leads-to-id-conflicts-and-a-link-misses-on-web)
  - [Tags show up twice under scopes](#tags-show-up-twice-under-scopes)
  - [Skip absolute link exit check on web](#skip-absolute-link-exit-check-on-web)
  - [Prop dangerouslySetInnerHtml did not match on some pages](#prop-dangerouslysetinnerhtml-did-not-match-on-some-pages)
  - [Self links broken on /ciro-santilli starting at Budget transparency](#self-links-broken-on-ciro-santilli-starting-at-budget-transparency)
  - [Don't move to a separate page when clicking link to image to another header that is already visible on current page on web](#don-t-move-to-a-separate-page-when-clicking-link-to-image-to-another-header-that-is-already-visible-on-current-page-on-web)
  - [Don't move to a separate page when clicking toc links in a page that has scope on web](#don-t-move-to-a-separate-page-when-clicking-toc-links-in-a-page-that-has-scope-on-web)
  - [Wiki link on same line as parent link on web h1](#wiki-link-on-same-line-as-parent-link-on-web-h1)
  - [h1 arguments broken on web](#h1-arguments-broken-on-web)
  - [Capture link clicks to headers in current page and don't change page](#capture-link-clicks-to-headers-in-current-page-and-don-t-change-page)
  - [Remove word count on web](#remove-word-count-on-web)
  - [Fix ToC links on web, missing scope](#fix-toc-links-on-web-missing-scope)
- [Tags](#tags)
  - [DB](#db)
  - [File](#file)
    - [File autogen](#file-autogen)
  - [Metadata section](#metadata-section)
  - [Elements](#elements)
    - [Image](#image)
    - [Math](#math)
    - [Table](#table)
    - [Header](#header)
      - [Synonym](#synonym)
  - [UI](#ui)
    - [Firefox](#firefox)
    - [CSS](#css)
  - [Web](#web)
    - [Web upload](#web-upload)
    - [Comment](#comment)
    - [Dynamic tree fetch](#dynamic-tree-fetch)
    - [Editor](#editor)
    - [Error checking](#error-checking)
    - [Include](#include)
    - [Issue](#issue)
    - [Offline development](#offline-development)
    - [Topic](#topic)
  - [CLI](#cli)
  - [Word count](#word-count)
  - [Lib](#lib)
    - [Tag](#tag)
  - [Bug](#bug)
  - [Scope](#scope)
  - [Performance](#performance)
  - [Publicity](#publicity)
  - [Publish](#publish)
  - [Refactor](#refactor)
  - [ToC](#toc)

## Issues

↑ **Parent:** [TODO](todo.md)

### Encrypted client hello

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_2"></a>
One day we'll enable it, e.g. with Cloudfare:<a id="_3"></a>

<a id="_4"></a>
- [https://developers.cloudflare.com/support/third-party-software/others/configure-cloudflare-and-heroku-over-https/](https://developers.cloudflare.com/support/third-party-software/others/configure-cloudflare-and-heroku-over-https/)
<a id="_5"></a>
- [https://developers.cloudflare.com/ssl/edge-certificates/ech/](https://developers.cloudflare.com/ssl/edge-certificates/ech/)

### Add button on web to move article to trash on web

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_7"></a>
Having the same effect as whatever we decide to make [Section "Move articles deleted locally to under a trash article on web"](#move-articles-deleted-locally-to-under-a-trash-article-on-web) do.

### Convert ordered list Ol to a boolean argument of unordered lists Ul

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [File autogen](#file-autogen)

<a id="_9"></a>
We are better than HTML, we have arguments! This is just a style matter, HTML was wrong to add it to content model.

### Allow linking to auto-generated files

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [File autogen](#file-autogen)

<a id="_11"></a>
It would be cool if we could do:<a id="_12"></a>

```
<myfile.txt>{file}
```
when there is a file `myfile.txt` without a corresponding `{file}` header such as:<a id="_13"></a>

```
= myfile.txt
{file}
```
As of writing, on static we already autogenerate such `_file` pages for all files (not yet on web but we should too), so it's just a matter of checking if the target file exists when the ID doesn't for error checking, and linking to the \_file.

<h3 id="link-to-file-rather-than-raw-if-there-s-split-pages">Link to _file rather than _raw if there's split pages</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [File autogen](#file-autogen)

<a id="_15"></a>
E.g.:<a id="_16"></a>

```
= path/to/myfile.txt
{file}
```
would generate a breadcrumb like:<a id="_17"></a>

```
(root)/path/to/<myfile.txt>{file}{split}
```
where `{split}` is a possibly new argument that ensures it links to split if there are split pages, and not the current:<a id="_18"></a>

```
(root)/path/to/\a[myfile.txt]
```
This would make [file autogen](#file-autogen) much more useful and visible. The general premise is that we should link to split `{file}` preferentially always.

<a id="_19"></a>
Pre-requisite: [Allow linking to auto-generated files](#allow-linking-to-auto-generated-files)

### Show directory listings on `{file}` headers

↑ **Parent:** [Issues](#issues)

<a id="_20"></a>
Like big files, only show on split pages.

<a id="_21"></a>
Once this is done, we can entirely replace the custom directory listing generated in the `ourbigbook` executable by it, which will be the exact same code path as `{file}` generation.

<a id="_22"></a>
Closely related issue: [https://github.com/ourbigbook/ourbigbook/issues/348](https://github.com/ourbigbook/ourbigbook/issues/348)

<h3 id="5">Nested set index corruption</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Bug](#bug), [Web](#web)

<a id="_25"></a>
There is an outstanding nested set index corruption going on which hasn't been identified yet. Running on Heroku:<a id="_26"></a>

```
web/bin/rerender-articles.js
```
blew up with:<a id="_27"></a>

```
cirosantilli/simply-connected-space
cirosantilli/simulation
/app/web/convert.js:459
        throw new ValidationError(`the parent choice "${newParentId}" would create an infinite loop`)
              ^

ValidationError
    at /app/web/convert.js:459:15
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async /app/web/node_modules/sequelize/dist/lib/sequelize.js:463:24
    at async Object.convertArticle (/app/web/convert.js:176:3)
    at async /app/web/models/article.js:844:9
    at async /app/web/node_modules/sequelize/dist/lib/sequelize.js:463:24
    at async Article.rerender (/app/web/models/article.js:842:5)
    at async Article.rerender (/app/web/models/article.js:1615:9)
    at async /app/web/bin/rerender-articles.js:19:1 {
  info: undefined,
  errors: 'the parent choice "@cirosantilli/conceptual-model" would create an infinite loop',
  status: 422
}
```
and the DB check:<a id="_28"></a>

```
heroku run web/bin/normalize -c nested-set -u cirosantilli
```
failed with:<a id="_29"></a>

```
AssertionError [ERR_ASSERTION]: nested-set: (slug, nestedSetIndex, nestedSetNextSibling, depth): actual: (cirosantilli/natural-science, 419, 3414, 2) !== expected: (@cirosantilli/natural-science, 419, 3411, 2)
    at Object.normalize (/app/web/models/index.js:400:20)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async /app/web/bin/normalize:28:3 {
  generatedMessage: false,
  code: 'ERR_ASSERTION',
  actual: 3414,
  expected: 3411,
  operator: 'strictEqual'
}
```

<a id="_30"></a>
The local source corresponding to that was:<a id="_31"></a>

```
= Conceptual model
{parent=Scientific method}
{wiki}

= Model
{synonym}

= Simulation
{parent=Conceptual model}
{wiki}
```
and it hadn't changed in a long time according to git log, also:<a id="_32"></a>

```
= Natural science
{parent=Science}
{wiki}

...

= Thermo Electron
{c}
{parent=Thermo Fisher Scientific}
{title2=1956-}
{wiki}

= Natural science YouTube channel
{parent=Natural science}
{wiki}

= The Thought Emporium
{c}
{parent=Natural science YouTube channel}
{wiki}

\Include[linguistics]{parent=science}

...

= Scientific method
{parent=Science}
{wiki}
```
are three consecutive siblings.

<a id="_33"></a>
Some related database lines via:<a id="_34"></a>

```
bin/psql -A -F' ' <<EOF >db.tmp
select "nestedSetIndex","nestedSetNextSibling",slug from "Article" where slug like 'cirosantilli/%' order by "nestedSetIndex"
EOF
```
are:<a id="_35"></a>

```
  419 | 3414 | cirosantilli/natural-science

 3411 | 3412 | cirosantilli/thermo-electron
 3412 | 3414 | cirosantilli/natural-science-youtube-channel
 3413 | 3414 | cirosantilli/the-thought-emporium
 3414 | 3553 | cirosantilli/linguistics

 3551 | 3553 | cirosantilli/chinese-slang
 3552 | 3553 | cirosantilli/shabi
 3553 | 3864 | cirosantilli/scientific-method
```
Humm, that index looks correct, what's going on?

<a id="_36"></a>
I hack:<a id="_37"></a>

```

@@ -392,6 +392,7 @@ async function normalize({
         const articles = await Article.treeFindInOrder({ username, transaction })
         if (check) {
           const nestedSetsFromRefs = await Article.getNestedSetsFromRefs(username, { transaction })
+          nestedSetsFromRefs.map(e => console.error(`${e.nestedSetIndex} ${e.nestedSetNextSibling} ${e.id}`))
```
and see:<a id="_38"></a>

```
3550 3864 @cirosantilli/scientific-method
```
There's an offset of 3 somewhere!

<a id="_39"></a>
OK the first glaring error in the DB is social science right in the middle of physics things:<a id="_40"></a>

```
1497 1498 cirosantilli/physx
1500 1801 cirosantilli/social-science
1501 1503 cirosantilli/3d-ridig-body-dynamics-benchmark
1502 1503 cirosantilli/simbenchmark
```
Also [https://ourbigbook.com/cirosantilli/social-science](https://ourbigbook.com/cirosantilli/social-science) gave 500.

<a id="_41"></a>
Possibly related:<a id="_42"></a>

```
1501 1503 cirosantilli/3d-ridig-body-dynamics-benchmark
```
was a recent change, and part of this complex source code move that can be simplified to:<a id="_43"></a>

```
--- a/science.bigb
+++ b/science.bigb
@@ -345,40 +345,7 @@ https://www.youtube.com/watch?v=H_H_TF5Kxks This Lab is RIDICULOUS (2021) gives
-= 3D physics engine
-{parent=Physics engine}
-{tag=3D}
-
-= 3D physics engine benchmark
-{parent=3D physics engine}
```
to:<a id="_44"></a>

```
@@ -512,3 +512,117 @@ This idealization does not seems to be possible at all in the context of <Maxwel
 = Rigid body
 {parent=Point particle}
 {wiki}
+
+= Rigid body dynamics
+{parent=Rigid body}
+
+= 3D rigid body dynamics
+{parent=Rigid body dynamics}
+{tag=3D}
+
+= 3D rigid body dynamics simulator
+{parent=3D rigid body dynamics}
+
+= 3D physics engine
+{synonym}
+
+= PhysX
+{c}
+{parent=3D rigid body dynamics simulator}
+{tag=C++ library}
+
+= 3D ridig body dynamics benchmark
+{parent=3D rigid body dynamics}
+
+= 3D physics engine benchmark
+{synonym}
+
+= SimBenchmark
+{parent=3D ridig body dynamics benchmark}
```
so it contains two simultaneous renames, before:<a id="_45"></a>

```
= 3D physics engine
  = 3D physics engine benchmark
```
after:<a id="_46"></a>

```
= 3D rigid body dynamics
  = 3D rigid body dynamics simulator (3D physics engine)
    = PhysX
  = 3D rigid body dynamics benchmark (3D physics engine benchmark)
    = SimBenchmark
```
Gotta try to make a minimal test reproduction for this mess.

### Like and unlike requests are very slow

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Performance](#performance), [Web](#web)

<a id="_49"></a>
On ourbigbook.com like and unlike takes 4s-10s! Something is wrong. It must be because of the complex side effects like topic updating? Maybe those should be deferred? This only appears noticeable on a larger database.

<a id="_50"></a>
Edit: as of today it was taking 500 ms, so likely some index was added that improved it a lot.

### Incoming links and tagged metadata does not show synonyms

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Metadata section](#metadata-section), [Synonym](#synonym)

<a id="_53"></a>
Both CLI and web. E.g.:

<a id="_54"></a>
README.bigb<a id="_55"></a>

```
= Index

<notindex2>
```

<a id="_56"></a>
notindex.bigb<a id="_57"></a>

```
= Notindex

= Notindex2
{synonym}
```

<a id="_58"></a>
then:<a id="_59"></a>

```
ourbigbook .
```
the output notindex.html does not have an incoming links metadata section. With `<notindex>` it does have a metadata section. The outcome metadata section should be identical on both.

<a id="_60"></a>
Same for tags that use the synonym.

<a id="_61"></a>
Added a test now for it.

### Image title with x to image with content incorrectly disallowed

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Lib](#lib)

<a id="_63"></a>
Should only blow up if the `\\x` does not have a content explicitly set. See broken test `cross reference from image title to previous non-header with content is allowed`.

<a id="_64"></a>
To fix we need to store some extra data on the Ref or Id table that determines if the reference needs the title or not to determine its own ID.

### Lint tables for correct number of columns

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Lib](#lib), [Table](#table)

<a id="_67"></a>
Maybe there is a valid use case for rows with different number of columns. But likely by default we should error unless the use explicitly allows this.

<h3 id="remove-synonym-from-json-use-ref-type-synonym-instead">Remove synonym from JSON, use Ref.type = synonym instead</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Refactor](#refactor), [Web](#web)

<a id="_70"></a>
When hydrating JSON asts from server we just need to do that extra join.

### Forbid uppercase IDs on web and CLI by default

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

### Option to add view on ourbigbook link on header metadata of CLI static renders

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<h3 id="4">Reorder convert to move Article.destroySideEffect before File.destroy</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Refactor](#refactor), [Web](#web)

### List synonyms on metadata section

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Synonym](#synonym)

<a id="_76"></a>
Edit: done for CLI. On web, showing just IDs to user to start with. Attempted to render on fly but failing for now. That's the only missing thing.

<a id="_77"></a>
Both web and CLI.

<h3 id="web-header-metadata-to-widgets">Move all header metadata from source to HTML in Web</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_79"></a>
This is way more user friendly. We have currently done that for `parent=` which would be:<a id="_80"></a>

```
= Calculus
{parent=Mathematics}
```
but now is just set on the Web UI.

<a id="_81"></a>
But we should likely do this for every other metadata, e.g.:<a id="_82"></a>

<a id="_83"></a>
- `synonym`
<a id="_84"></a>
- `id`
<a id="_85"></a>
- `scope`
<a id="_86"></a>
- `title2`
<a id="_87"></a>
- `c`
and so on.

### Fix parentId and previousSiblingId on articles API

↑ **Parent:** [Issues](#issues)

<a id="_88"></a>
The underlying reason is that:<a id="_89"></a>

```
.getArticles({includeParentAndPreviousSibling: true
```
is broken. The singular version `getArticle` however is not.

<h3 id="ref-file-normalization">Id, Ref and File foreign normalization</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [DB](#db)

<a id="_91"></a>
We've started noticing this as we went along and became more familiar with proper database design:<a id="_92"></a>

<a id="_93"></a>
- Ref.from\_id and to\_id should point to Id
<a id="_94"></a>
- File should be removed when deleted: [https://github.com/ourbigbook/ourbigbook/issues/216](https://github.com/ourbigbook/ourbigbook/issues/216) Currently this can only happen locally. Edit: will also start happening on upstream with synonym moves.
<a id="_95"></a>
- toplevel\_id<a id="_96"></a>

  <a id="_97"></a>
  - File.toplevel\_id should point to an Id object via primary key. Currently done via idid text.
  <a id="_98"></a>
  - Id.toplevel\_id should point to an Id object. No links at all apparently.
<a id="_99"></a>
- Article.topicId should point to Topic.id, not be TEXT

<a id="_100"></a>
We could then consider removing several `Ref.destroy` and `Id.destroy` `ON CASCADE` with `File` and `Id`, rather than manually.

<h3 id="web-create-multiple-headers">Allow creation of multiple headers in one go on web</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_102"></a>
Implemented for new articles: the editor splits the input with the same `split_headers` conversion used by `ourbigbook --web`, then creates each article in parent-before-child order. Editing an existing article remains single-header.

### Option to add zip of local conversion to converted GitHub pages website

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Publish](#publish)

<a id="_104"></a>
Would be cool, easily allowing full website download for offline viewing! One day.

<h3 id="3">Cross source file word count is always 0 on ToC hover</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Word count](#word-count)

<h3 id="1">Internal cross reference to non-existent ID is not checked before render the second time we try to convert</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Bug](#bug), [Error checking](#error-checking)

<a id="_108"></a>
README.bigb<a id="_109"></a>

```
= Index

<asdf>
```
Then the first:<a id="_110"></a>

```
ourbigbook .
```
fails as desired before any rendering takes place:<a id="_111"></a>

```
extract_ids: README.bigb
extract_ids: README.bigb finished in 45.4546590000391 ms
error:
README.bigb:3:2: cross reference to unknown id: "asdf"
```
Then the second:<a id="_112"></a>

```
ourbigbook .
```
fails differently, incorrectly trying to render but failing:<a id="_113"></a>

```
extract_ids: README.bigb
extract_ids: README.bigb skipped by timestamp
render: README.bigb
error: README.bigb:3:2: cross reference to unknown id: "asdf" at render time
copy README.bigb -> out/html/_raw/README.bigb
render: README.bigb -> out/html/index.html finished in 51.55012200027704 ms
```
with an error at render time.

<a id="_114"></a>
This is especially noticeable/confusing when you are converting a large number of files, and the second run will start converting a large number of files instead of failing early, until it eventually reaches the error when rendering the specific file.

<a id="_115"></a>
The key code point is:<a id="_116"></a>

```
async function check_db(sequelize, paths_converted, { transaction }) {
```
We are only checking the DB for the paths converted, but then due to parse skipping we skip the paths and don't check them anymore.

<a id="_117"></a>
Instead, we should check the entire database.

<a id="_118"></a>
The question then is: is there a way to do this efficiently with a query, without bringing the entire Refs database into memory, notably conisdering inflections?

### Add a `File:` prefix to `{file}` headers

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [File](#file)

<a id="_120"></a>
And also to full links, at least on ToC.

### Allow `{parent}` to point to `{file}` header

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [File](#file)

<a id="_122"></a>
```
= my/file.txt

= Asdf
{parent=my/file.txt}
{parentFile}
```

<a id="_123"></a>
Same for tags.

<a id="_124"></a>
Currently there is some confusion in the code on treating the `<>{file}` like the file in `= Header{file}`: one if about pointing to things, the other is about the current thing. We will disambiguate with `parentFile`.

<a id="_125"></a>
Same for `tag` and `tagFile`.

<a id="_126"></a>
It is currently possible however to just do:<a id="_127"></a>

```
= .gitignore

= child
{parent=_file/.gitignore}
```
I need to think why it works.

### Show likers list on article page

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

### Show like and follow date on user like follow lists

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<h3 id="handle-email-replies-to-notification-at-ourbigbook-com">Handle email replies to notification@ourbigbook.com</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<h3 id="firefox-tab-lists-don-t-wrap">Firefox tab lists don't wrap</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Firefox](#firefox), [Web](#web)

<a id="_133"></a>
On Firefox 109, tab lists such as those in the home page don't wrap if the screen is narrow.

<a id="_134"></a>
This is due to:<a id="_135"></a>

```
.tab-item: { white-space: pre }
```
but does not make much sense, as it should only take effect inside `.tab-item`, not on the `.tab-list` itself, feels like a firefox bug.

<a id="_136"></a>
We want the `white-space: pre` so that tab entries won't be broken up across lines.

<a id="_137"></a>
Works fine in Chromium 109.

<a id="_138"></a>
TODO can't reproduce on a minimal HTML page, so anoying!!!<a id="_139"></a>

```
<!doctype html>
<html lang=en>
<head>
<meta charset=utf-8>
<title>Min sane</title>
<style>
span {
  white-space: pre;
}
</style>
</head>
<body>
  <span>My item 1</span>
  <span>My item 2</span>
  <span>My item 3</span>
  <span>My item 4</span>
  <span>My item 5</span>
  <span>My item 6</span>
  <span>My item 7</span>
  <span>My item 8</span>
  <span>My item 9</span>
  <span>My item 10</span>
  <span>My item 11</span>
  <span>My item 12</span>
  <span>My item 13</span>
  <span>My item 14</span>
  <span>My item 15</span>
  <span>My item 16</span>
  <span>My item 17</span>
  <span>My item 18</span>
  <span>My item 19</span>
</body>
</html>
```

### Follow topic

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Topic](#topic), [Web](#web)

<a id="_142"></a>
This is one of those things that require a smart algorithm otherwise it will be quickly useless.

### At mention and topics on web

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_144"></a>
Currently on web:<a id="_145"></a>

<a id="_146"></a>
- `<@user-name>` produces a working link, but with bad title "index"
<a id="_147"></a>
- `<#some-topic>` fails

<a id="_148"></a>
What we want to work is either of:<a id="_149"></a>

<a id="_150"></a>
- `@user-name`
<a id="_151"></a>
- `#some-topic`
<a id="_152"></a>
- `<#some topic>`

<a id="_153"></a>
Perfect topic rendering can be a bit trick because it might require fetching actual topic from DB to see its preferred title.

<a id="_154"></a>
At mentions ideally bring the side-effect of notifications, but then we have to think about spam a bit too.

### At mention and topics locally

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_156"></a>
The constructs from [at mention and topics on web](#at-mention-and-topics-on-web) should also just work locally, and redirect to ourbigbook.com by default.

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

### View article and issue likers and followers

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Issue](#issue), [Web](#web)

### Like comments

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Issue](#issue), [Web](#web)

### Use same parent title if the current user has a matching article when clicking "Create my own version of article" 

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Topic](#topic), [Web](#web)

### Delete article

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_167"></a>
This is a bit hard to to properly as it requires checking that a billion dependant objects are also deleted:<a id="_168"></a>

<a id="_169"></a>
- issues
<a id="_170"></a>
- comments of those issues
<a id="_171"></a>
- file
<a id="_172"></a>
- IDs defined in that article
<a id="_173"></a>
- change the parentId of all chidren to the parent article of the deleted article, and also updated nested set index
Some of those can go on cascades, but others will require side-effects.

<a id="_174"></a>
Related:<a id="_175"></a>

<a id="_176"></a>
- [https://github.com/ourbigbook/ourbigbook/issues/216](https://github.com/ourbigbook/ourbigbook/issues/216)

### Serialize parsed build-in KaTeX macros

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Math](#math)

<a id="_178"></a>
I.e. save the output of `katex.renderToString` to JSON or some other format. This approach would ensure minimal load times no matter what KaTeX is doing, and possibly provide some good portability.

<a id="_179"></a>
Off the bat `JSON.stringify` doesn't work due to circular references though that can be overcome: [https://stackoverflow.com/questions/10392293/stringify-convert-to-json-a-javascript-object-with-circular-reference](https://stackoverflow.com/questions/10392293/stringify-convert-to-json-a-javascript-object-with-circular-reference)

### Handle web upload after local article renaming with synonym redirection set

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_182"></a>
Web upload breaks with duplicate ID if you rename a header and synonym the old one.

<a id="_183"></a>
TODO this issue is the same as: [https://github.com/ourbigbook/ourbigbook/issues/319](https://github.com/ourbigbook/ourbigbook/issues/319)?

### Photos of the merchandise!

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Publicity](#publicity)

### Flyers

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Publicity](#publicity)

<h3 id="ourbigbook-com-web-uploads-sometimes-fail-with-etimedout-or-econnreset">ourbigbook.com --web uploads sometimes fail with ETIMEDOUT or ECONNRESET</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Bug](#bug), [Web upload](#web-upload)

<a id="_188"></a>
ourbigbook --web sometimes randomly times out on ourbigbook.com. First an ID extraction or render hangs, and then after a few seconds things blow up Usually happens around the thousands of articles uploaded.

<a id="_189"></a>
I've seen it happen once or twice locally as well.

<a id="_190"></a>
There are no server exceptions on `heroku logs`. I simply can't understand why it happens.

<a id="_191"></a>
Once the error was `ETIMEDOUT`, but most times it was `ECONNRESET`.

<a id="_192"></a>
<a id="_193"></a>
- [https://stackoverflow.com/questions/17245881/how-do-i-debug-error-econnreset-in-node-js](https://stackoverflow.com/questions/17245881/how-do-i-debug-error-econnreset-in-node-js)

<a id="_194"></a>
Next time it happens I'm just going to add a timeout plus retry mechanism as it is rare enough that it shouldn't matter, and the problem does seem to go away if I try to continue the upload immediately afterwards: given the SHA2-based skips, restarting from the CLI we just start exactly where we had left off, so hopefully will also work from Js.

### Header followed by paragraph without blank line does not split correctly

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Bug](#bug)

<a id="_196"></a>
README.bigb

<a id="_197"></a>
```
= Asdf

== Qwer
zxcv
```

<a id="_198"></a>
then:

<a id="_199"></a>
```
ourbigbook --split-headers README.bigb
```

<a id="_200"></a>
leads to `out/html/split.html` that contains the `Qwer` header, and no `qwer.html` output.

<a id="_201"></a>
This construct should just be forbidden by linting instead forcing the preferred:

<a id="_202"></a>
```
= Asdf

== Qwer

zxcv
```

<a id="_203"></a>
Similar problem with preceding paragraph:

<a id="_204"></a>
README.bigb

<a id="_205"></a>
```
= Asdf

zxcv
== Qwer
```

<a id="_206"></a>
The root failure case in both cases is that the header goes inside the paragraph.

<a id="_207"></a>
Hmm, perhaps that is not a bad behavior... OK so going back a bit further, the problem is the outcome of:<a id="_208"></a>

```
ourbigbook --web .
```
on such cases, which leads to errors.

<h3 id="store-sha-of-each-article-plus-descendants-and-skip-api-re-renders-for-entire-subtrees">Store SHA of each article + descendants and skip API re-renders for entire subtrees</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_211"></a>
This is one step beyond [skip re-render from API if article was unchanged](#skip-re-render-from-api-if-article-was-unchanged) as it removes the requirement of actually uploading thousands of lines of content.

<a id="_212"></a>
It requires negotiating with the server instead.

<a id="_213"></a>
This would be particularly powerful if we included the descendants on the SHA of each parent, much like Git. This way we could skip enter unmodified subtrees, likely like Git.

<a id="_214"></a>
Yes, we are somewhat re-implementing parts of Git with this. But at least it is simple, and works at a sub-blob level given our grater specialization to our specific use case.

### Multiheader editing

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_216"></a>
Maybe we should only do this after: [https://github.com/ourbigbook/ourbigbook/issues/248](https://github.com/ourbigbook/ourbigbook/issues/248) to prevent data loss.

<a id="_217"></a>
One possibility is to prevent deletion/renaming of headers. We could just check the new ID list agains the previous ID list.

<a id="_218"></a>
This was possible previously on Web, but we forbade it for simplicity of implementation sake.

<a id="_219"></a>
We can then think about how the UI would look like, there might be a "Edit article and descendants" button on toplevel only for example.

### Make open and close arrows have the same height on ToC

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [ToC](#toc), [UI](#ui)

<a id="_222"></a>
Otherwise the difference in ToC line entry spacing is very unnerving.

<h3 id="add-sibling-add-child-buttons-next-to-toc-entries-of-articles-owned-by-the-current-user">Add sibling/add child buttons next to toc entries of articles owned by the current user</h3>

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [ToC](#toc), [Web](#web)

<a id="_225"></a>
Self headers done. ToC missing.

### Progress spinner after submit

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [UI](#ui), [Web](#web)

<a id="_228"></a>
[Article create and update slow on web](#article-create-and-update-slow-on-web) was an extreme case of slowness, but it taught us that we do want some kind of immediate feedback as soon as users click a form submission, and one feedback blocks further action such as typing.

### Hide unconfirmed users

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_230"></a>
Will likely get solved via: [https://github.com/ourbigbook/ourbigbook/issues/329](https://github.com/ourbigbook/ourbigbook/issues/329)

### Fragment redirects not working on web

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_232"></a>
E.g. [https://ourbigbook.com/cirosantilli/mathematics#cirosantilli/physics](https://ourbigbook.com/cirosantilli/mathematics#cirosantilli/physics) should redirect to [https://ourbigbook.com/cirosantilli/physics](https://ourbigbook.com/cirosantilli/physics)

<a id="_233"></a>
Is working on static website: [https://cirosantilli.com/mathematics#physics](https://cirosantilli.com/mathematics#physics) does redirect to [https://cirosantilli.com/physics](https://cirosantilli.com/physics)

### WYSIWYG

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Editor](#editor), [Web](#web)

### Live error checking as you type on editor if chosen previous sibling is not a child of the selected parent article

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Editor](#editor), [Error checking](#error-checking), [Web](#web)

<a id="_239"></a>
Current failure behavior if use submits anyways is: shows API error `previousSiblingId "@cirosantilli/physics" does not exist, is not a header or is not a child of parentId "@cirosantilli/test-article"` under title, and it only goes away if you edit title, which is confusing as it is not title related. Also, while title error is visible, the submit button is inactive so the user is left a bit stuck.

### Reach the same performance as static website with dynamic tree

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Performance](#performance), [Web](#web)

<a id="_242"></a>
The move to dynamic tree slowed things down a lot for large pages such as: [https://ourbigbook.com/cirosantilli](https://ourbigbook.com/cirosantilli), making it is just unacceptably slow, and actually blocks any other page loads as the server does work.

<a id="_243"></a>
These were at cirosantilli.github.io at aa60ccb934bf9646d548e6b761489d31aec1a341, which has almost 7k articles.

<a id="_244"></a>
Some benchmarks on Chromium:<a id="_245"></a>

<a id="_246"></a>
- `ping cirosantilli.com`: 17 ms
<a id="_247"></a>
- [https://cirosantilli.com](https://cirosantilli.com) `GET /`: 1.3s. Waiting for server: ping time only, the rest is content download. `content-length` from response: 300 kB zipped.
<a id="_248"></a>
- [https://ourbigbook/cirosantilli](https://ourbigbook/cirosantilli) `GET /`:<a id="_249"></a>

  <a id="_250"></a>
  - Waiting for server response: 3.5s to 4s. That's our problem!
  <a id="_251"></a>
  - Contend download: 2.5s
<a id="_252"></a>
- [http://localhost:3000/cirosantilli](http://localhost:3000/cirosantilli) `npm run dev` `GET /`:<a id="_253"></a>

  <a id="_254"></a>
  - <a id="_255"></a>
    Waiting for server response: between 2 and 3s. So we reproduce relatively well locally.

    <a id="_256"></a>
    curl `time_starttransfer` after a few stabilizing runs: 2.6s
  <a id="_257"></a>
  - Contend download: 1.6s

<a id="_258"></a>
If we comment the single line in Article.tsx:<a id="_259"></a>

```
//html += renderTocFromEntryList({ entry_list })
```
TTFB falls from 2.6s to 0.77s.

<a id="_260"></a>
Removing the `renderRefCallback` drops it to between 2.2 and 2.4.

<a id="_261"></a>
Limiting the ToC to 1k articles on server side leads to 0.5s. Maybe that's the first workaround we have to do until something else is understood. It is a shame that we have to go so much lower than the static website.

<a id="_262"></a>
Maybe we can use some of the techniques from: [https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists](https://reactjs.org/docs/optimizing-performance.html#virtualize-long-lists) to improve things.

### Inject React header metadata on each header separately

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_264"></a>
This is closely related to: [Reach the same performance as static website with dynamic tree](#reach-the-same-performance-as-static-website-with-dynamic-tree). Performance considerations should guide if we actually want this or not.

<a id="_265"></a>
No more need for:<a id="_266"></a>

```
for (const h of elem.querySelectorAll('.h')) {
```
on `Article.tsx` now that we have separate headers, we can just inject it one by one.

<a id="_267"></a>
Bibliography:

<a id="_268"></a>
<a id="_269"></a>
- [https://stackoverflow.com/questions/44643424/how-to-parse-html-to-react-component](https://stackoverflow.com/questions/44643424/how-to-parse-html-to-react-component)
<a id="_270"></a>
- [https://stackoverflow.com/questions/36104302/how-do-i-convert-a-string-to-jsx](https://stackoverflow.com/questions/36104302/how-do-i-convert-a-string-to-jsx)
<a id="_271"></a>
- [https://stackoverflow.com/questions/71224517/is-it-possible-to-inject-a-next-js-component-into-an-existing-application-html](https://stackoverflow.com/questions/71224517/is-it-possible-to-inject-a-next-js-component-into-an-existing-application-html)

### Include should work transparently with README in subdirectory

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Include](#include), [Web](#web)

<a id="_274"></a>
We should be able to write:

<a id="_275"></a>
animal.bigb<a id="_276"></a>

```
= Animal

\Include[dog]
```

<a id="_277"></a>
dog/README.bigb<a id="_278"></a>

```
= Dog
```

<a id="_279"></a>
since the dog.bigb file should ideally be fully equivalent to

<a id="_280"></a>
dog.bigb<a id="_281"></a>

```
= Dog
{scope}
```

### Remove the path parameter from the article creation API

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_283"></a>
Edit: a use case has come up for this: if we can find an existing article that the user is trying to update, we might be able to determine that it does not need to be converted in the first place: [skip re-render from API if article was unchanged](#skip-re-render-from-api-if-article-was-unchanged). But then of course we can't render the article to find its ID, as the hole point is to skip that render in the first place.

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

### Statically render links to issues and topic under each header for better SEO

↑ **Parent:** [Issues](#issues)  
🏷️ **Tags:** [Web](#web)

<a id="_296"></a>
The links don't show without JavaScript, this can be seen by disabling Js.

<a id="_297"></a>
The counts can be dynamic loaded, but the links we really want to do at compile time... any way?

## Make rendered issue and comment fragments as short as possible

↑ **Parent:** [TODO](todo.md)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

<a id="_300"></a>
For now I made them almost fully correct AFAIS:<a id="_301"></a>

<a id="_302"></a>
- no ID conflicts that would show on the same page, e.g. across issue IDs and comment IDs
<a id="_303"></a>
- links seem to go to where we want them to

<a id="_304"></a>
The only known bug is: [cannot link from comment to article](#cannot-link-from-comment-to-article)

<a id="_305"></a>
However, in order to achieve this easily we used scopes liberally, and so the fragments are horrendously long.

<a id="_306"></a>
The ideal fragment setup for both comments and issues would be either:<a id="_307"></a>

<a id="_308"></a>
- we don't ever want to show multiple comments/issues from different issues on same page<a id="_309"></a>

  <a id="_310"></a>
  - issue IDs:<a id="_311"></a>

    <a id="_312"></a>
    - regular elements `my-header`
    <a id="_313"></a>
    - ToC IDs<a id="_314"></a>

      <a id="_315"></a>
      - the ToC: `_toc`
      <a id="_316"></a>
      - the links: `_toc/my-header`
  <a id="_317"></a>
  - comment IDs:<a id="_318"></a>

    <a id="_319"></a>
    - regular elements `_comment/1/my-header`
    <a id="_320"></a>
    - ToC IDs<a id="_321"></a>

      <a id="_322"></a>
      - the ToC: `_comment/1/_toc`
      <a id="_323"></a>
      - the links: `_comment/1/_toc/my-header`
<a id="_324"></a>
- we want to show multiple comments/issues from different issues on same page:<a id="_325"></a>

  <a id="_326"></a>
  - issue IDs:<a id="_327"></a>

    <a id="_328"></a>
    - regular elements `_issue/barack-obama/article-topic/1/my-header`
    <a id="_329"></a>
    - ToC IDs<a id="_330"></a>

      <a id="_331"></a>
      - the ToC: `_issue/barack-obama/article-topic/1/_toc`
      <a id="_332"></a>
      - the links: `_issue/barack-obama/article-topic/1/_toc/my-header`
  <a id="_333"></a>
  - comment IDs:<a id="_334"></a>

    <a id="_335"></a>
    - regular elements `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/my-header`
    <a id="_336"></a>
    - ToC IDs<a id="_337"></a>

      <a id="_338"></a>
      - the ToC: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc`
      <a id="_339"></a>
      - the links: `_comment/barack-obama/article-topic/<issue-id>/<comment-id>/_toc/my-header`

## Cannot link from comment to article

↑ **Parent:** [TODO](todo.md)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

<a id="_342"></a>
[https://github.com/ourbigbook/ourbigbook/issues/277](https://github.com/ourbigbook/ourbigbook/issues/277)

<a id="_343"></a>
As of now, does work with a leading slash: `</test data>`.

<a id="_344"></a>
Also: it does work if there is a header in the comment before the link.

### Clicking on the comment header does not highlight the header line

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

<a id="_347"></a>
By that we mean the hardcoded `#n` area with the metadata, not an h1.

<a id="_348"></a>
However if you refresh the page, it highlights! Mystery.

### Comment h1 self link is empty and thus refreshes the page

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

### Remove all unnecessary newlines from HTML output

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Lib](#lib)

<a id="_352"></a>
These newlines were added for debugging purposes, but debugging should just be done with:<a id="_353"></a>

```
npx js-beautify min.html
```

<a id="_354"></a>
Newlines just add complexity to our codebase, and are not even getting removed from final output as things stand to take up a little bit of useless space.

### ToC link on headers not opening collapsed toc entries

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Bug](#bug)

### parentId dropdown autocomplete

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Web](#web)

### LIKE metadata on JOIN on

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)

<a id="_357"></a>
<a id="_358"></a>
- web descendants
<a id="_359"></a>
- all article lists

### Load more articles

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Web](#web)

<a id="_362"></a>
Either with scroll or a load more button. Slightly tempted by a load more button?

<a id="_363"></a>
To implement, we just have to expose the ArticlePage.ts fetch in an API manner. The page then tracks current limit on a state variable, and just requests more from that point onwards.

<a id="_364"></a>
Starting from the commit of this line, we are also going to limit the ToC, so a load more button on ToC would also be of interest: [load more ToC entrie](#load-more-toc-entrie).

### Load more ToC entrie

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Web](#web)

### Word count on web

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Web](#web), [Word count](#word-count)

<a id="_369"></a>
Likely also at same time do a source character count.

<a id="_370"></a>
Likely would be easy to implement as it would reuse the exact same query that we already use to update ncestors of the nested set index.

<a id="_371"></a>
Was removed at: [remove word count on web](#remove-word-count-on-web) because would require actually implementing properly but lazy.

<a id="_372"></a>
We should likely not show it on link hover however, only headers, as doing so would mean having to update every single page that links to a header for correctness. If this is ever done, it should be Js runtime stuff only.

### Monaco editor requires web

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)  
🏷️ **Tags:** [Editor](#editor), [Offline development](#offline-development), [Web](#web)

<a id="_376"></a>
It seems that the third party library we are using is just a hack and doesn't properly provide the thing offline... OMG could it be so crap? [https://stackoverflow.com/questions/59773190/monaco-editor-with-nextjs/68611592#68611592](https://stackoverflow.com/questions/59773190/monaco-editor-with-nextjs/68611592#68611592)

<h3 id="respect-ourbigbook-json-htmlxextension-on-ourbigbook-json-redirects">Respect ourbigbook.json <code>htmlXExtension</code> on ourbigbook.json redirects</h3>

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)

<a id="_377"></a>
Would require either moving `htmlXExtension` vs `--no-html-x-extension` processing out of `index.js`, or more ideally moving the redirection generation into index.js.

<a id="_378"></a>
But aint't nobody got time for that!

### iframe macro

↑ **Parent:** [Cannot link from comment to article](#cannot-link-from-comment-to-article)

<a id="_379"></a>
Reasonable results can already be obtained with:  
\<iframe src="\_raw/js/matterjs/examples.html\#top-down-asdw-fixed-viewport" width="1000" height="850"\>\</iframe\>  
The main issue with that is the possibly changing `_raw/js/matterjs/examples.html` path depending on scopes, and it is also not very nice to have to write `_raw` explicitly.

<a id="_380"></a>
Instead we should do the same handling as is currently done for `\a[]` and `\Image[]` on these paths.

## Closed issues

↑ **Parent:** [TODO](todo.md)

### Allow disambiguate and id header arguments on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope), [Web](#web)

<a id="_383"></a>
Currently these do not affect the article's ID as there is a fundamental limitation of the `convert` function, which determines the "file path" based solely on the title content, and ignores the title arguments such as `disambiguate`. The ID of the first header, the toplevel ID, then just gets fixed to that (as is meant to happen, first toplevel gets Id fixed), ignoring `disambiguate`.

<a id="_384"></a>
This is worked around on web upload by passing the `id` as the `path` explicitly as an argument. But this argument is not available on web UI, and it would be ugly anyways, what we want is for it to "just work" by default without the user having to explicitly set an ID on web UI.

<a id="_385"></a>
Fixed at: 56e8d17aa1b716ce69689c6b8aaae0acf4804421 web: fix editing for articles with ID modifiers like scope or disambiguate

### Remove scope from toc entry IDs

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [CLI](#cli), [Scope](#scope)

<a id="_388"></a>
Happens on CLI and Web, though the web one is a bit artificial.

<a id="_389"></a>
E.g. [https://cirosantilli.com/x86-paging#toc-x86-paging/sample-code](https://cirosantilli.com/x86-paging#toc-x86-paging/sample-code) should instead be just: [https://cirosantilli.com/x86-paging#toc-sample-code](https://cirosantilli.com/x86-paging#toc-sample-code). Links from headers to currently work however.

<a id="_390"></a>
On web will require extra caution after we decided to initially stop culling scopes: [missing header metadata such as like button, same topic and issue link on headers under a scope](#missing-header-metadata-such-as-like-button-same-topic-and-issue-link-on-headers-under-a-scope).

<a id="_391"></a>
Edit: this was fixed on web after we did the insane and amazing dynamic tree JavaScript redirects: [https://ourbigbook.com/cirosantilli/x86-paging#_toc/sample-code](https://ourbigbook.com/cirosantilli/x86-paging#_toc/sample-code) But we never got round to fixing it on static where it still goes to the bad [https://cirosantilli.com/x86-paging#_toc/x86-paging/sample-code](https://cirosantilli.com/x86-paging#_toc/x86-paging/sample-code)

<h3 id="split-and-nosplit-links-missing-from-cirosantilli-com">split and nosplit links missing from cirosantilli.com</h3>

↑ **Parent:** [Closed issues](#closed-issues)

<a id="_392"></a>
[https://cirosantilli.com/brazilian-music-split](https://cirosantilli.com/brazilian-music-split) doesn't have nosplit

### Move articles deleted locally to under a trash article on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_394"></a>
During `--web` upload.

<a id="_395"></a>
The exact name of that article is a somewhat difficult question, if we go non-magical then:<a id="_396"></a>


> My deleted articles

will do. But we could go more magical:<a id="_397"></a>

```
_my/trash
```
or polluting a bit without `_`:<a id="_398"></a>

```
my/trash
```
Perhaps such a namespace would be useful for stuff like `my/contact`, `my/body`, `my/hardware` and so on.

<a id="_399"></a>
Edit: we decided to create unlisted articles rather than doing this.

### Vs Code symbol provider

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Visual Studio Code](README.md#visual-studio-code)

<a id="_401"></a>
Allow you to Ctrl + Click on any internal link such as `\x[]` and jump to the corresponding header.

<a id="_402"></a>
[https://code.visualstudio.com/api/language-extensions/programmatic-language-feature](https://code.visualstudio.com/api/language-extensions/programmatic-language-feature)

<a id="_403"></a>
We'd just use the SQLite database with some exiting wrapper function most likely. Hardest part is likely calculating the target ID.

### Allow creating new pages under scope on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope), [Web](#web)

<a id="_406"></a>
This casually started working without us noticing much after 3f4e7594ea5d28c3b30a0b7e874ca4627849cbea made parent selection a bit more accurate for scopes. Hurray.

<a id="_407"></a>
We likely just have to set the `path:` API argument based on the has scope status of the parent article.

<a id="_408"></a>
As of the commit that adds this line, it should likely be possible to do it on the backend. On the frontend however we convert `/` to `-` so it doesn't work on the existence checks. We need a more accurate ID conversion there.

### Show tagged list of non toplevel pages

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Tag](#tag)

<a id="_410"></a>
Both web and CLI.

### Shorthand block quotes

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

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

### ToC Js folding broken on Web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug), [ToC](#toc), [Web](#web)

<a id="_430"></a>
Working on static.

<h3 id="allow-user-to-edit-other-user-s-articles">Allow user to edit other user's articles</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_432"></a>
Curently impossible on the API level: it just takes the logged in user and uses that as the new/edit target.

<a id="_433"></a>
Current use case: allow admin to edit other user's articles e.g. as part of moderation.

### Blowup with unclosed image followed by math

↑ **Parent:** [Closed issues](#closed-issues)

<a id="_434"></a>
```
= Index

\Image[qwer

$$
asdf
$$
```

### Ordered list lost when rendering to bigb output format

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [`Bigb` output format](README.md#bigb-output-format)

<a id="_436"></a>
Added a commented out test to [test_bigb_output.bigb](test_bigb_output.bigb):<a id="_437"></a>

```
\Ol[
* p1
* p2
]
```
renders to just:<a id="_438"></a>

```
* p1
* p2
```
Also it might be possible to get an extra newline due to this which breaks web upload, but we don't have a min repro currently.

### Render large files on split headers

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [File](#file)

<a id="_440"></a>
Currently files that are large don't render in either multi nor split headers.

<a id="_441"></a>
But instead we want it to render on split headers because the \_raw version does not always show on GitHub pages, but rather gets downloaded which is bad.

<a id="_442"></a>
The `{file}` version is also cool as it allows easy navigation to other files, and comments to be added.

<a id="_443"></a>
This is currently not so easy to implement because things are done at the ast tree level rather than at render time, which is bad. So the same ast ends up going for both split and nosplit renders.

<h3 id="remove-synthetic-asts">Don't use helper synthetic AST nodes, render at render time instead</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [File](#file), [Refactor](#refactor)

<a id="_446"></a>
This is a hard refactor that likely will never be done. But so be it.

### View article source on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_448"></a>
Can start simple with either raw or contained, and then add both some day. GitHub copy.

### Benchmark and optimize output size

↑ **Parent:** [Closed issues](#closed-issues)

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

### Web upload fails when renaming a header to a synonym

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web upload](#web-upload)

<a id="_458"></a>
First:

<a id="_459"></a>
test-data.bigb<a id="_460"></a>

```
= Test data

== Tmp
```
then:<a id="_461"></a>

```
ourbigbook --web-test
```

<a id="_462"></a>
Then modify to:<a id="_463"></a>

```
= Test data

== Tmp2

= Tmp
```
and rerun:<a id="_464"></a>

```
ourbigbook --web-test
```

<a id="_465"></a>
Error message:<a id="_466"></a>

```
param "bodySource" is mandatory when not rendering or when "path" to an existing article is not given. path="tmp"
```

<a id="_467"></a>
Can be worked around by:<a id="_468"></a>

```
rm -rf out
```
therefore it is just a case of some outdated local state, thank God for that, should be simple to fix.

<a id="_469"></a>
The root problem seems to be that `sqlite3 _out/web/web.sqlite3 .dump` still contains `tmp`, we have to get rid of any synonym headers during ID extraction.

### Render ancestors, incoming links and tagged on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_471"></a>
All dynamic.

### Vertical scrollbar when image title contains math underscore

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [CSS](#css)

<a id="_473"></a>
Only happens when the title would fit in a single line:<a id="_474"></a>

```
\Image[https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/BSD_data_plot_for_elliptic_curve_800h1.svg/640px-BSD_data_plot_for_elliptic_curve_800h1.svg.png]
{title=$a_b$}
{height=400}
```

<a id="_475"></a>
For long titles that go over a single line, it doesn't happen.

<a id="_476"></a>
Removing from `ourbigbook.scss`:<a id="_477"></a>

```
figure {
  overflow-x: auto;
```
fixes for some reason, but breaks everything else, as it adds a global vertical scrollbar to the page if there are any images wider than it (when above the mobile mode where images are just width 100%.

<a id="_478"></a>
The fundamental issue seems to be: [https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue](https://stackoverflow.com/questions/6421966/css-overflow-x-visible-and-overflow-y-hidden-causing-scrollbar-issue) which we don't know how to work around. Omg.

<a id="_479"></a>
To get a clearer effect edit ourbigbook.scss to:<a id="_480"></a>

```
.katex { font-size: 20.2em; }
```
Only the separation between `a` and its subscript `b` seems to matter.

### Make articles removed locally empty on web upload

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_483"></a>
Otherwise the following sequence leads to a hard to understand failure for the end user.

<a id="_484"></a>
First the user uploads with:

<a id="_485"></a>
```
== Header 1

== Header 2

\Image[img.png]{title=My image}
```

<a id="_486"></a>
Then, `Header 2` is completely removed from all source files and the image is moved to `Header 1`:

<a id="_487"></a>
```
== Header 1

\Image[img.png]{title=My image}
```

<a id="_488"></a>
Then, when the use tries to upload again, it fails because of duplicated id `image-my-image`.

<a id="_489"></a>
This above sequence of events is not ideal from the users' perspective, as a synonym generation would lead to better URLs:

<a id="_490"></a>
```
== Header 1

= Header 2
{synonym}

\Image[img.png]{title=My image}
```

<a id="_491"></a>
In that sequence, the File for `Header 2` would be effectively emptied of Ids, and there would be no duplicates.

<a id="_492"></a>
But still, if the user deletes a header, it becomes very difficult to know it later on. So perhaps when the CLI downloads the SHA list, it could also check if there are articles on server that both:<a id="_493"></a>

<a id="_494"></a>
- are not present locally anymore
<a id="_495"></a>
- have a non-empty hash
and then proceed to make any such headers empty to avoid ID duplication.

<a id="_496"></a>
Aditionaly, it would also be good to move the deleted articles to some predefined header to avoid cluttering the headers. E.g. we could start with a dummy "My deleted articles". Dedicated section: [Section "Move articles deleted locally to under a trash article on web"](#move-articles-deleted-locally-to-under-a-trash-article-on-web).

<h3 id="don-t-skip-parent-previous-sibling-updates-on-web-uploads">Don't skip parent/previous sibling updates on --web uploads</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_499"></a>
We have recently implemented SHA-256 skips when article content hasn't changed.

<a id="_500"></a>
But we also need to check if the parent or previous sibling has changed, and if it has then update that.

<a id="_501"></a>
We could just return parent and previous sibling on the `/hash` endpoint.

<a id="_502"></a>
Or we need to add that information to the SHA.

<a id="_503"></a>
Ideally we should also have a way to change the tree without re-render, though we could start with re-render for simplicity.

<a id="_504"></a>
This actually breaks uploads because it leads to inconsistencies when finding previousSiblingId.

### CLI nosplit points to self

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [CLI](#cli), [Web upload](#web-upload)

<a id="_507"></a>
E.g.: [https://cirosantilli.com/education-level](https://cirosantilli.com/education-level) nosplit points to the page itself. Should instead point to [https://cirosantilli.com/education#education-level](https://cirosantilli.com/education#education-level)

<a id="_508"></a>
Possiby happens only with:<a id="_509"></a>

```
  "publishOptions": {
    "toSplitHeaders": true,
    "htmlXExtension": false,
    "xPrefix": "https://ourbigbook.com/cirosantilli/"
  },
```
redirects enabled.

<a id="_510"></a>
Further investigation shows that `"toSplitHeaders": true,` is the issue. Fixing this for now bu ust removing the split/nosplit in that case.

### Pass previousSiblingId on web upload

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_513"></a>
Otherwise uploads become irreproducible if you stop half way. Unacceptable.

### Links to synonym header have fragment

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug), [Web](#web)

<a id="_516"></a>
E.g. from [https://ourbigbook.com/cirosantilli/ciro-santilli](https://ourbigbook.com/cirosantilli/ciro-santilli):<a id="_517"></a>

```
<Python>
```
renders as:<a id="_518"></a>

```
/cirosantilli/python-programming-language#cirosantilli/python-programming-language
```
instead of the desired:<a id="_519"></a>

```
/cirosantilli/python-programming-language
```

<a id="_520"></a>
However the link to the non-synonym header:<a id="_521"></a>

```
<Python (programming language)>
```
renders correctly without the fragment

<a id="_522"></a>
OK, this was also reproducible on CLI, links to toplevel synonyms had fragments, just it is infinitely more visible on web where everything is toplevel.

### Put raw files in a separate magic prefix

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [File](#file)

<a id="_524"></a>
We should have:<a id="_525"></a>

<a id="_526"></a>
- `_raw/path/to/main.py`: raw file
for every file `path/to/main.py` in the repo to avoid URL clashes, e.g. between:<a id="_527"></a>

```
configure
configure.bigb
```

<a id="_528"></a>
Will also serve as a mechanism to view .bigb source without GitHub.

### Synonym redirects on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

### Start a basic notification system

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_531"></a>
OK, now after the big redirect from cirosantilli.com to ourbigbook.com, this is becoming more pressing.

<a id="_532"></a>
We could start simple without any in-browser things, email only. Though having both would be ideal...

<h3 id="2">Find a way to show index.html raw files that get overriden by directory listings</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [File](#file)

<a id="_534"></a>
Edit: first implemented the `_index` thing. But actually noticed would be saner with a separate `_dir/` prefix for directories. Otherwise a recursive wget/zip would not work out of box which makes me sad. It is a bit sad that you can't just remove a path from `_raw/path/to/file.txt` to go to `_raw/path/to/` as you need `_dir/path/to/` instead. But so bet it.

<a id="_535"></a>
E.g. `subdir/index.html` which would show up under `_raw/subdir/index.html` gets overriden by the directory listing of `subdir/` which goes to the same location.

<a id="_536"></a>
One possibility would be to add an underscore: `_raw/subdir/_index.html` for the file. And another underscore for `_index.html` and so on.

<h3 id="automatically-add-source-to-archive-org-images">Automatically add <code>source</code> to archive.org images</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Image](#image)

<a id="_538"></a>
E.g. [https://web.archive.org/web/20230227073734im_/https://upload.wikimedia.org/wikipedia/commons/2/2b/STED_Mikroskop_PSFs.jpg](https://web.archive.org/web/20230227073734im_/https://upload.wikimedia.org/wikipedia/commons/2/2b/STED_Mikroskop_PSFs.jpg) to [https://upload.wikimedia.org/wikipedia/commons/2/2b/STED_Mikroskop_PSFs.jpg](https://upload.wikimedia.org/wikipedia/commons/2/2b/STED_Mikroskop_PSFs.jpg).

<a id="_539"></a>
Edit: OK that is useless. The source needs to be an HTML page, and we can't infer that from the archive links. Manual sources are necessary in that case.

### Put files in a separate namespace

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [File](#file)

<a id="_541"></a>
We should have:<a id="_542"></a>

<a id="_543"></a>
- `_file/path/to/main.py`: OurBigBook section showing preview of file + comments/metadata
<a id="_544"></a>
- `_raw/path/to/main.py`: raw file
Done the `_file` part.

### Following and followed tabs are swapped

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

### Undefined tag error message for directory conversion says header ID is not defined instead of tag ID

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug), [Tag](#tag)

<a id="_548"></a>
README.bigb<a id="_549"></a>

```
= Tmp

== Tmp 2
{tag=adsf}
```
convert:<a id="_550"></a>

```
ourbigbook .
```
outcome:<a id="_551"></a>

```
extract_ids: README.bigb
extract_ids: README.bigb finished in 43.47357300110161 ms
error:
README.bigb:4:1: cross reference to unknown id: "tmp-2"
```
expected outcome:<a id="_552"></a>

```
README.bigb:4:1: cross reference to unknown id: "asdf"
```

### Design a project banner

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Publicity](#publicity)

<a id="_554"></a>
E.g. for Twitter and LinkedIn.

<a id="_555"></a>
Maybe a screenshot of the website?

<a id="_556"></a>
If we could represent topics somehow that would be ideal...

### Subsections missing on web dynamic tree

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug), [Dynamic tree fetch](#dynamic-tree-fetch)

<a id="_559"></a>
Going to close it for now as irreproducible. Worked around it by fixing data manualy with the new `nested-set` CLI tool. Will try to debug further if it shows up again in the future.

<a id="_560"></a>
On web now:<a id="_561"></a>

<a id="_562"></a>
- [https://ourbigbook.com/barack-obama](https://ourbigbook.com/barack-obama) shows Fundamental theorem of calculus under "Integral", correct
<a id="_563"></a>
- [https://ourbigbook.com/barack-obama/mathematics](https://ourbigbook.com/barack-obama/mathematics) does not show "Fundamental theorem of calculus", incorrect

<a id="_564"></a>
We can only reproduce locally by copying the database, we haven't managed to reach such state by a clean sequence of pure API calls, clean naive `web/bin/generate-demo-data -C -u1` didn't reproduce either.

<a id="_565"></a>
Upon quickly inspectig the DB we see that the nested set indexes are wrong:<a id="_566"></a>

```
[ 'barack-obama', 0, 36 ],
[ 'barack-obama/mathematics', 1, 9 ],
[ 'barack-obama/fundamental-theorem-of-calculus', 9, 11 ],
```
`barack-obama/mathematics` should stop something larger than `9` to include `barack-obama/fundamental-theorem-of-calculus` and other children.

<a id="_567"></a>
The question is now if this is still reachable, of if it was due to a previous bug.

### Enable web math defines default on non-web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Math](#math), [Web](#web)

<a id="_570"></a>
This is the only way to have portable maths across local and server.

<a id="_571"></a>
The definitions are also useful by default to users, and should just be enabled out-of-box.

### Enable web math defines on web editor

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Editor](#editor), [Math](#math), [Web](#web)

<a id="_575"></a>
They're not enabled there, conversion just fails and user can't submit because button is grayed out. Via API already works however, supposing the user has defined them: [enable web math defines default on non-web](#enable-web-math-defines-default-on-non-web).

### Store auto-formated bigb source on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug)

<a id="_577"></a>
Edit: caching only fails if you edit on web, then somehow download it and change and reupload. But change implies rerender. Hard to see a case where this actually causes problems.

<a id="_578"></a>
We are auto-formatting locally for splitting and to get rid of includes.

<a id="_579"></a>
So we need to also format on web in order for content caching to work.

<h3 id="split-out-bigb-and-out-web">Split _out/bigb and _out/web</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug)

<a id="_581"></a>
Currently:<a id="_582"></a>

```
ourbigbook --web
```
stores the split renders under:<a id="_583"></a>

```
out/bigb
```
since it is a bigb output.

<a id="_584"></a>
However, that bigb output is different from the one gnerated with:<a id="_585"></a>

```
ourbigbook -O bigb .
```
since the latter contains `\Include` which need to be removed from the `web/` output.

### Skip re-render from API if article was unchanged

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web), [Web upload](#web-upload)

<a id="_588"></a>
Would radically speed sync up.

### Computer sticker

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Publicity](#publicity)

### Prevent full page reload on links using our existing link capture

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_591"></a>
Would be a possibly good solution now to: [https://github.com/ourbigbook/ourbigbook/issues/274](https://github.com/ourbigbook/ourbigbook/issues/274) now that we already have link click capturing necessarily.

### Second meta line showing up on index page even if empty

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_593"></a>
Index has no parent, so the line may be empty in that case.

### Article create and update slow on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Performance](#performance), [Web](#web)

<a id="_596"></a>
[https://ourbigbook.com/api/articles](https://ourbigbook.com/api/articles)

<a id="_597"></a>
For user cirosantilli, just pushed cirosantilli.github.io at aa60ccb934bf9646d548e6b761489d31aec1a341, which has almost 7k articles.

<a id="_598"></a>
The POST to [https://ourbigbook.com/api/articles](https://ourbigbook.com/api/articles) is taking about 3s to 4s on ourbigbook.com "Waiting for server response", 3.44s seems like an common average exact value that often comes back.

<a id="_599"></a>
This was after dynamic article tree, one suspicion is that it might be linked to maintaining the nested set state on a large set of articles. I really hope that's not it, as it would be hard to fix.

<a id="_600"></a>
Doing it from the `barack-obama` test user which only has about 50 articles leads to the same result, but we believe it is because we are not indexing things by user properly (this was added later), so might still be due to nested set.

<a id="_601"></a>
Locally on sqlite is only 800 ms to 900 ms.

<a id="_602"></a>
Locally on postgresql with `barack-obama` user and no `cirosantilli` data, the POST is almost instantaneous however... 100ms or less!

<a id="_603"></a>
Local postgresql with `cirosantilli` user after uploading cirosantilli.github.io with about 7k articles: usually around 2.4s, sometimes a bit less.

<a id="_604"></a>
Same but with `barack-obama`: 2.16s! So the main slowdown is likely that we are not properly indexing things, as one users' article affects the other's!

<a id="_605"></a>
Let's hack it up to see:<a id="_606"></a>

```
./bin/psql
alter table "Article" add "authorId" integer;
update "Article" as a set "authorId" = f."authorId" from "File" as f where a."fileId" = f.id
create index idx_nested ON "Article" using btree ("authorId", "nestedSetIndex");
```

<a id="_607"></a>
and patch:

<a id="_608"></a>
```
diff --git a/web/convert.js b/web/convert.js
index 59870ae3..ff834708 100644
--- a/web/convert.js
+++ b/web/convert.js
@@ -568,6 +568,7 @@ async function convertArticle({
         const rendered_output = extra_returns.rendered_outputs[outpath]
         const renderFull = rendered_output.full
         articleArgs.push({
+          authorId: file.authorId,
           depth: newDepth,
           fileId: file.id,
           h1Render: renderFull.substring(0, rendered_output.h1RenderLength),
@@ -599,6 +600,7 @@ async function convertArticle({
         articleArgs,
         {
           updateOnDuplicate: [
+            'authorId',
             'h1Render',
             'h2Render',
             'titleRender',
diff --git a/web/models/article.js b/web/models/article.js
index 40dbbdba..1c382acc 100644
--- a/web/models/article.js
+++ b/web/models/article.js
@@ -13,6 +13,10 @@ module.exports = (sequelize) => {
     'Article',
     {
       // E.g. `johnsmith/mathematics`.
+      authorId: {
+        type: DataTypes.INTEGER,
+        allowNull: false,
+      },
       slug: {
         type: DataTypes.TEXT,
         unique: {
```

<a id="_609"></a>
Didin't help :-(

<a id="_610"></a>
A cleaner benchmarking can now be done with:<a id="_611"></a>

```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -C -u1 -a650 -i0 -c0
```
By this size, things are already unreasonably slow, and you can visibly see the latter renders being much slower than the early ones. We can then do a very minimal one off benchmark of a single slow article update with:<a id="_612"></a>

```
OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -u1 -a1 -i0 -c0
```
OK, now the test case is clearer.

<a id="_613"></a>
By also enabling SQL logging:<a id="_614"></a>

```
time DEBUG='*:sql:*' OURBIGBOOK_POSTGRES=1 ./bin/generate-demo-data.js -u1 -a1 -i0 -c0
```
which gave:<a id="_615"></a>

```
real    0m1.400s
user    0m0.643s
sys     0m0.068s
```
we will be able to see any slow queries. We reach the following two massively slow queries:<a id="_616"></a>

```
SELECT
  "Ref".*,
  "to"."id" AS "to.id",
  "to"."idid" AS "to.idid",
  "to"."path" AS "to.path",
  "to"."toplevel_id" AS "to.toplevel_id",
  "to"."ast_json" AS "to.ast_json",
  "to"."macro_name" AS "to.macro_name",
  "to"."createdAt" AS "to.createdAt",
  "to"."updatedAt" AS "to.updatedAt",
  "to->File"."id" AS "to.File.id",
  "to->File"."path" AS "to.File.path",
  "to->File"."toplevel_id" AS "to.File.toplevel_id",
  "to->File"."last_parse" AS "to.File.last_parse",
  "to->File"."last_render" AS "to.File.last_render",
  "to->File"."titleSource" AS "to.File.titleSource",
  "to->File"."bodySource" AS "to.File.bodySource",
  "to->File"."createdAt" AS "to.File.createdAt",
  "to->File"."updatedAt" AS "to.File.updatedAt",
  "to->File"."authorId" AS "to.File.authorId",
  "to->File->file"."id" AS "to.File.file.id",
  "to->File->file"."slug" AS "to.File.file.slug",
  "to->File->file"."topicId" AS "to.File.file.topicId",
  "to->File->file"."titleRender" AS "to.File.file.titleRender",
  "to->File->file"."titleSource" AS "to.File.file.titleSource",
  "to->File->file"."titleSourceLine" AS "to.File.file.titleSourceLine",
  "to->File->file"."render" AS "to.File.file.render",
  "to->File->file"."h1Render" AS "to.File.file.h1Render",
  "to->File->file"."h2Render" AS "to.File.file.h2Render",
  "to->File->file"."depth" AS "to.File.file.depth",
  "to->File->file"."score" AS "to.File.file.score",
  "to->File->file"."nestedSetIndex" AS "to.File.file.nestedSetIndex",
  "to->File->file"."nestedSetNextSibling" AS "to.File.file.nestedSetNextSibling",
  "to->File->file"."createdAt" AS "to.File.file.createdAt",
  "to->File->file"."updatedAt" AS "to.File.file.updatedAt",
  "to->File->file"."fileId" AS "to.File.file.fileId",
  "from"."id" AS "from.id",
  "from"."idid" AS "from.idid",
  "from"."path" AS "from.path",
  "from"."toplevel_id" AS "from.toplevel_id",
  "from"."ast_json" AS "from.ast_json",
  "from"."macro_name" AS "from.macro_name",
  "from"."createdAt" AS "from.createdAt",
  "from"."updatedAt" AS "from.updatedAt",
  "from->File"."id" AS "from.File.id",
  "from->File"."path" AS "from.File.path",
  "from->File"."toplevel_id" AS "from.File.toplevel_id",
  "from->File"."last_parse" AS "from.File.last_parse",
  "from->File"."last_render" AS "from.File.last_render",
  "from->File"."titleSource" AS "from.File.titleSource",
  "from->File"."bodySource" AS "from.File.bodySource",
  "from->File"."createdAt" AS "from.File.createdAt",
  "from->File"."updatedAt" AS "from.File.updatedAt",
  "from->File"."authorId" AS "from.File.authorId",
  "from->File->file"."id" AS "from.File.file.id",
  "from->File->file"."slug" AS "from.File.file.slug",
  "from->File->file"."topicId" AS "from.File.file.topicId",
  "from->File->file"."titleRender" AS "from.File.file.titleRender",
  "from->File->file"."titleSource" AS "from.File.file.titleSource",
  "from->File->file"."titleSourceLine" AS "from.File.file.titleSourceLine",
  "from->File->file"."render" AS "from.File.file.render",
  "from->File->file"."h1Render" AS "from.File.file.h1Render",
  "from->File->file"."h2Render" AS "from.File.file.h2Render",
  "from->File->file"."depth" AS "from.File.file.depth",
  "from->File->file"."score" AS "from.File.file.score",
  "from->File->file"."nestedSetIndex" AS "from.File.file.nestedSetIndex",
  "from->File->file"."nestedSetNextSibling" AS "from.File.file.nestedSetNextSibling",
  "from->File->file"."createdAt" AS "from.File.file.createdAt",
  "from->File->file"."updatedAt" AS "from.File.file.updatedAt",
  "from->File->file"."fileId" AS "from.File.file.fileId"
FROM
  (
    SELECT
      "Ref"."id",
      "Ref"."type",
      "Ref"."from_id",
      "Ref"."to_id",
      "Ref"."defined_at",
      "Ref"."defined_at_line",
      "Ref"."defined_at_col",
      "Ref"."inflected",
      "Ref"."to_id_index",
      "Ref"."createdAt",
      "Ref"."updatedAt"
    FROM
      "Ref" AS "Ref"
    WHERE
      "Ref"."to_id" = '@barack-obama/test-data'
      AND "Ref"."type" = 0
    LIMIT
      1
  ) AS "Ref"
  LEFT OUTER JOIN "Id" AS "to" ON "Ref"."to_id" = "to"."idid"
  LEFT OUTER JOIN "File" AS "to->File" ON "to"."idid" = "to->File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "to->File->file" ON "to->File"."id" = "to->File->file"."fileId"
  LEFT OUTER JOIN "Id" AS "from" ON "Ref"."from_id" = "from"."idid"
  LEFT OUTER JOIN "File" AS "from->File" ON "from"."idid" = "from->File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "from->File->file" ON "from->File"."id" = "from->File->file"."fileId";

+451ms

SELECT
  "Id".*,
  "File"."id" AS "File.id",
  "File"."path" AS "File.path",
  "File"."toplevel_id" AS "File.toplevel_id",
  "File"."last_parse" AS "File.last_parse",
  "File"."last_render" AS "File.last_render",
  "File"."titleSource" AS "File.titleSource",
  "File"."bodySource" AS "File.bodySource",
  "File"."createdAt" AS "File.createdAt",
  "File"."updatedAt" AS "File.updatedAt",
  "File"."authorId" AS "File.authorId",
  "File->file"."id" AS "File.file.id",
  "File->file"."slug" AS "File.file.slug",
  "File->file"."topicId" AS "File.file.topicId",
  "File->file"."titleRender" AS "File.file.titleRender",
  "File->file"."titleSource" AS "File.file.titleSource",
  "File->file"."titleSourceLine" AS "File.file.titleSourceLine",
  "File->file"."render" AS "File.file.render",
  "File->file"."h1Render" AS "File.file.h1Render",
  "File->file"."h2Render" AS "File.file.h2Render",
  "File->file"."depth" AS "File.file.depth",
  "File->file"."score" AS "File.file.score",
  "File->file"."nestedSetIndex" AS "File.file.nestedSetIndex",
  "File->file"."nestedSetNextSibling" AS "File.file.nestedSetNextSibling",
  "File->file"."createdAt" AS "File.file.createdAt",
  "File->file"."updatedAt" AS "File.file.updatedAt",
  "File->file"."fileId" AS "File.file.fileId"
FROM
  (
    SELECT
      "Id"."id",
      "Id"."idid",
      "Id"."path",
      "Id"."toplevel_id",
      "Id"."ast_json",
      "Id"."macro_name",
      "Id"."createdAt",
      "Id"."updatedAt"
    FROM
      "Id" AS "Id"
    WHERE
      "Id"."idid" = '@barack-obama'
    LIMIT
      1
  ) AS "Id"
  LEFT OUTER JOIN "File" AS "File" ON "Id"."idid" = "File"."toplevel_id"
  LEFT OUTER JOIN "Article" AS "File->file" ON "File"."id" = "File->file"."fileId"

+227m
```
Hmmm, so no slow updates, only selects. Surprising!

<a id="_617"></a>
The first query is the:<a id="_618"></a>

```
const oldRef = await sequelize.models.Ref.findOne({
```

<a id="_619"></a>
OK, we manually reduced the first query to a subset:<a id="_620"></a>

```
SELECT
  "Ref"."to_id",
  "Ref"."from_id",
  "From"."idid" AS "From.idid",
  "From->File"."titleSource" AS "From->File.titleSource"
FROM "Ref"
INNER JOIN "Id" AS "From"
ON
  "Ref"."from_id" = "From"."idid" AND
  "Ref"."to_id" = '@barack-obama/test-data' AND
  "Ref"."type" = 0
INNER JOIN "File" AS "From->File"
  ON "From"."idid" = "From->File"."toplevel_id"
INNER JOIN "Article" AS "From->Article"
  ON "From->File"."id" = "From->Article"."fileId"
;
```
which we were certain should not be slow, and then by commenting things out learnt that foreign keys are not automatically indexed, so the `fileId` finding was super slow!!! OMG.

<a id="_621"></a>
That single one line change drops us down to half the creation time, amazing:<a id="_622"></a>

```
real    0m0.668s
user    0m0.638s
sys     0m0.035s
```

<a id="_623"></a>
On heroku, after manually doing:<a id="_624"></a>

```
create index article_file_id ON "Article" using btree ("fileId");
```
new article time fell down to 400ms, which is amazing. One liner! Special thanks to sequelize for the timing info.

<a id="_625"></a>
After this, the only DB activity that has more than 15ms is:<a id="_626"></a>

```
sequelize:sql:pg Executing (default): SELECT "id", "username", "ip", "displayName", "email", "image", "hash", "salt", "score", "followerCount", "admin", "verified", "verificationCode", "verificationCodeSent", "maxArticles", "maxArticleSize", "createdAt", "updatedAt" FROM "User" AS "User" WHERE "User"."username" = 'barack-obama'; +53ms
```
but we don't reproduce it in isolation, must be something else in play, e.g. something in parallel.

#### Article create and update slow on web update 1

↑ **Parent:** [Article create and update slow on web](#article-create-and-update-slow-on-web)

<a id="_627"></a>
As of this commit did a bit further investigation with a better tooling and more understanding, notably now we run:<a id="_628"></a>

```
OURBIGBOOK_LOG_DB=1 num run dev-pg
```

<a id="_629"></a>
Heroku is definitely slower than local, at around 1 t o2 s on the bit first ten pages:<a id="_630"></a>

```
ourbigbook --web --web-force-render --web-max-renders 10
```
but local was also rather slow when we have about the same number of articles for the user.

<a id="_631"></a>
After some improved benchmarking setup, there seem to be two separate causes:<a id="_632"></a>

<a id="_633"></a>
- <a id="_634"></a>
  preventing: `options.db_provider.fetch_header_tree_ids(` on web. It is not necessary as we render the ToC dynamically.

  <a id="_635"></a>
  This matters the most for toplevel articles with many descendants.
<a id="_636"></a>
- <a id="_637"></a>
  the other problem we haven't solved yet: the nested index update querries are slow. We don't know how to solve that easily.

  <a id="_638"></a>
  Those querries simply update a huge number of rows.

  <a id="_639"></a>
  Maybe we could have a fallback mechanism to build that index on the background, and use the tree index temporarily?

  <a id="_640"></a>
  Hard call.

### Donate button on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

### `(beta)` on navbar gets pushed down half way at a specific page width just above mobile shift

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [CSS](#css), [Web](#web)

<a id="_644"></a>
Just keep making viewport smaller an smaller, until it happen. Sample width that reproduces: 680px.

<a id="_645"></a>
Removing `white-space: pre-wrap` solves it. But then the space between `(beta)` and `OurBigBook.com` gets removed.

<a id="_646"></a>
OK: found out I had already previously solved the same issue with `&nbsp;`, redoing the "hack". Every header space has to be `&nbsp;`.

### Empty Latest Followed shows as There are no articles on this website yet

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<h3 id="add-sibling-add-child-buttons-next-to-headers-owned-by-the-current-user">Add sibling/add child buttons next to headers owned by the current user</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

### Infinite navbar profile image refresh loop when there is no Internet

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Offline development](#offline-development)

<a id="_650"></a>
This might be something to do with us trying to have a dummy fallbak image when the image URL does not exist.

<a id="_651"></a>
The request is:<a id="_652"></a>

```
GET https://static.productionready.io/images/smiley-cyrus.jpg net::ERR_INTERNET_DISCONNECTED
```
so it appears to be trying to infinitely fetch the default image.

<a id="_653"></a>
For now we seem to have managed to stop it from going infinite by selecting an image that is stored locally in the website.

### Separate lines with field label for parent and previous sibling on web editor

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Editor](#editor), [Web](#web)

<a id="_656"></a>
Otherwise too confusing what is what when fields are pre-filled, e.g. when editing existing, and in the future when clicking a "add here" button.

### Allow showing article body on article lists

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_658"></a>
Maybe some will be list by default, but some will definitely be article show by default. Notably topic has to show the rendered body by default.

<a id="_659"></a>
This is a superset of: [https://github.com/ourbigbook/ourbigbook/issues/270](https://github.com/ourbigbook/ourbigbook/issues/270)

### Comment h1 has empty metadata line where likes would be placed

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

<a id="_662"></a>
Likes will not go under header which does not need to be present, so gonna remove it.

### Comment autogenerated IDs are wrong when there is header in the comment

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

### Add an option to add a prefix to every ID of rendered output to avoid conflicts across comments and issue

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Comment](#comment), [Web](#web)

<a id="_667"></a>
[https://github.com/ourbigbook/ourbigbook/issues/251](https://github.com/ourbigbook/ourbigbook/issues/251)

<a id="_668"></a>
We noticed this is hard to implement, because we want internal links to still work, and just adding a prefix to every ID does not take that into account.

<a id="_669"></a>
We later noticed that what we actually want to solve the comment use case, is a custom toplevel scope, which we can easily implement with a custom named directory. So... scopes save the day for once?

<a id="_670"></a>
Will be useful for comments on web, since a single author can make multiple comments, so prefixing by usernme won't be enough.

<a id="_671"></a>
For topic pages, we can just prefix by username, and that is already currently done.

### First on-hover heder self link after table of content activates table of contents instead of header 

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_673"></a>
E.g.: [https://cirosantilli.com/physics#how-to-teach-and-learn-physics](https://cirosantilli.com/physics#how-to-teach-and-learn-physics)

<a id="_674"></a>
Broken ToC HTML render?

<a id="_675"></a>
OK, understood the root cause: we moved to rendering the ToC from inside the H rendering function itself, and as a result there is a single toplevel\_child\_modifier which acts on that entire output.

<a id="_676"></a>
We'll need to create something more custom to properly handle this case.

### h2 on hover self links are empty on Web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_678"></a>
And therefore lead users to the toplevel page instead of a link to current header.

<a id="_679"></a>
The links by clicking on the header itself are correct and go to a dedicated page with it on top. The problem is just for the on-hover links on the margin which we'd like to link to self in the current page.

### Test scope 2 appears after Test scope 1 on generated data

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_681"></a>
OK, everything was reversed, I just hadn't noticed before because there was no numbered test data :-)

<h3 id="prefix-unnumbered-ids-with-the-parent-header-s-id">Prefix unnumbered IDs with the parent header's ID</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Web](#web)

<h3 id="remove-at-from-toc-ids">Remove @ from toc IDs</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_685"></a>
E.g. currently have: [http://localhost:3000/barack-obama#toc-@barack-obama/mitochondrion](http://localhost:3000/barack-obama#toc-@barack-obama/mitochondrion) It works, but is ugly.

### Missing header metadata such as like button, same topic and issue link on headers under a scope

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope)

<h3 id="headers-under-scope-don-t-have-scope-on-id-leads-to-id-conflicts-and-a-link-misses-on-web">Headers under scope don't have scope on ID leads to ID conflicts and a link misses on Web</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope), [Web](#web)

<a id="_689"></a>
E.g. in:<a id="_690"></a>

```
= x86

== Sample code

== x86 paging
{scope}

=== Sample code
```

<a id="_691"></a>
both `Sample code` headers have `id="sample-code"`, which would lead to ID conflicts on the same page.

<a id="_692"></a>
Also, as a result, the toc link from `x86` intended to go to `x86-paging/sample-code` misses and opens on a separate page.

<a id="_693"></a>
I don't know how to solve this besides always including scopes on every ID... This does however lead to ugly local IDs on individual pages which is a bit of a shame... oh cruel life.

<a id="_694"></a>
We could also have two versions of every page, scoped and non scoped, but things likely go exponential when we start dealing with subscope.

<a id="_695"></a>
This could mean that a lot of toplevel scope removal work will go to the trash! :-( But what can you do, it is the inevitable outcome of dynamic page fetch?

### Tags show up twice under scopes

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope), [Web](#web)

<a id="_698"></a>
Happens on CLI, though was first noticed, and most important, on Web due to the all present user prefix.

<a id="_699"></a>
Was already fully present on the previous deployment but we just completely missed it, e.g.: [https://ourbigbook.com/cirosantilli/physics#physics-education-needs-more-focus-on-understanding-experiments-and-their-history](https://ourbigbook.com/cirosantilli/physics#physics-education-needs-more-focus-on-understanding-experiments-and-their-history)

<a id="_700"></a>
Minimal CLI example to reproduce:

<a id="_701"></a>
subdir/asdf.bigb

<a id="_702"></a>
```
= asdf
```

<a id="_703"></a>
subdir/qwer.bigb

<a id="_704"></a>
```
= qwer
{tag=asdf}
```

<a id="_705"></a>
Then in the rendering of `subdir/qwer.html`, the tag `asdf` appears twice.

<a id="_706"></a>
The root cause is that scope resolution is finding the same thing twice, one as `subdir/asdf` and then once again with just `asdf` (which is then correctly resolved).

### Skip absolute link exit check on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_708"></a>
Maybe: [https://stackoverflow.com/questions/10687099/how-to-test-if-a-url-string-is-absolute-or-relative](https://stackoverflow.com/questions/10687099/how-to-test-if-a-url-string-is-absolute-or-relative)

### Prop dangerouslySetInnerHtml did not match on some pages

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_710"></a>
Happens on some pages but not others, e.g. `barack-obama/ciro-santilli`.

<a id="_711"></a>
OK: that simply happens due to invalid HTML constructs:<a id="_712"></a>

<a id="_713"></a>
- [https://stackoverflow.com/questions/58266356/what-is-happening-such-i-receive-dangerouslysetinnerhtml-warning-and-empty-conte](https://stackoverflow.com/questions/58266356/what-is-happening-such-i-receive-dangerouslysetinnerhtml-warning-and-empty-conte)
<a id="_714"></a>
- [https://flaviocopes.com/react-fix-dangerouslysetinnerhtml-did-not-match/](https://flaviocopes.com/react-fix-dangerouslysetinnerhtml-did-not-match/)
and we had invalid or implicitly self closing HTML at: [self links broken on /ciro-santilli starting at Budget transparency](#self-links-broken-on-ciro-santilli-starting-at-budget-transparency).

### Self links broken on /ciro-santilli starting at Budget transparency

↑ **Parent:** [Closed issues](#closed-issues)

<a id="_715"></a>
There is some kind of fundamentally wrong HTML content being rendered, not Web specific: [https://cirosantilli.com/sponsor#budget-transparency](https://cirosantilli.com/sponsor#budget-transparency)

<a id="_716"></a>
Resolution: was due to missing a close tag that appeared when we used `\Quote` with `title`. It was even valid HTML OMG, but wront semantic. What a stack.

<h3 id="don-t-move-to-a-separate-page-when-clicking-link-to-image-to-another-header-that-is-already-visible-on-current-page-on-web">Don't move to a separate page when clicking link to image to another header that is already visible on current page on web</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<h3 id="don-t-move-to-a-separate-page-when-clicking-toc-links-in-a-page-that-has-scope-on-web">Don't move to a separate page when clicking toc links in a page that has scope on web</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Scope](#scope), [Web](#web)

### Wiki link on same line as parent link on web h1

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Web](#web)

<a id="_721"></a>
Likely locally too then right. Will also be more uniform with h2 which now has parent link.

<a id="_722"></a>
Also seems like empty line (no wiki) is showing: [http://localhost:3000/barack-obama/x86-paging/sample-code](http://localhost:3000/barack-obama/x86-paging/sample-code)

### h1 arguments broken on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Bug](#bug), [Web](#web)

<a id="_725"></a>
Both preview and render.

<a id="_726"></a>
OK, was not the arguments in general, was `{wiki}` alone with which I was testing, thank God!

<h3 id="capture-link-clicks-to-headers-in-current-page-and-don-t-change-page">Capture link clicks to headers in current page and don't change page</h3>

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Web](#web)

### Remove word count on web

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Web](#web), [Word count](#word-count)

<a id="_732"></a>
It is broken, and lazy to fix now.

<a id="_733"></a>
Can be fixed later at: [word count on web](#word-count-on-web).

### Fix ToC links on web, missing scope

↑ **Parent:** [Closed issues](#closed-issues)  
🏷️ **Tags:** [Dynamic tree fetch](#dynamic-tree-fetch), [Scope](#scope), [Web](#web)

<a id="_737"></a>
Fixed at: aca09f9485bcbc6c8cd184d61871f02e8a602981

## Tags

↑ **Parent:** [TODO](todo.md)

### DB

↑ **Parent:** [Tags](#tags)

<a id="_738"></a>
Database specific tasks, usually refactoring.

### File

↑ **Parent:** [Tags](#tags)

<a id="_739"></a>
This tag is about handling non-OurBigBook files, notably related to using the [`\H` `file` argument](README.md#h-file-argument).

#### File autogen

↑ **Parent:** [File](#file)

### Metadata section

↑ **Parent:** [Tags](#tags)

### Elements

↑ **Parent:** [Tags](#tags)

#### Image

↑ **Parent:** [Elements](#elements)

#### Math

↑ **Parent:** [Elements](#elements)

#### Table

↑ **Parent:** [Elements](#elements)

#### Header

↑ **Parent:** [Elements](#elements)

##### Synonym

↑ **Parent:** [Header](#header)

### UI

↑ **Parent:** [Tags](#tags)

#### Firefox

↑ **Parent:** [UI](#ui)

#### CSS

↑ **Parent:** [UI](#ui)

### Web

↑ **Parent:** [Tags](#tags)

#### Web upload

↑ **Parent:** [Web](#web)

<a id="_740"></a>
This tag is about `ourbigbook --web` uploading from the local filesystem to OurBigBook Web.

#### Comment

↑ **Parent:** [Web](#web)

#### Dynamic tree fetch

↑ **Parent:** [Web](#web)

#### Editor

↑ **Parent:** [Web](#web)

#### Error checking

↑ **Parent:** [Web](#web)

#### Include

↑ **Parent:** [Web](#web)

#### Issue

↑ **Parent:** [Web](#web)

#### Offline development

↑ **Parent:** [Web](#web)

#### Topic

↑ **Parent:** [Web](#web)

### CLI

↑ **Parent:** [Tags](#tags)

### Word count

↑ **Parent:** [Tags](#tags)

### Lib

↑ **Parent:** [Tags](#tags)

#### Tag

↑ **Parent:** [Lib](#lib)

### Bug

↑ **Parent:** [Tags](#tags)

### Scope

↑ **Parent:** [Tags](#tags)

### Performance

↑ **Parent:** [Tags](#tags)

### Publicity

↑ **Parent:** [Tags](#tags)

### Publish

↑ **Parent:** [Tags](#tags)

### Refactor

↑ **Parent:** [Tags](#tags)

### ToC

↑ **Parent:** [Tags](#tags)

## ↑ Ancestors (1)

1. [OurBigBook Project](README.md)
