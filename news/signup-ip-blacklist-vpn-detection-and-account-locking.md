# Signup IP blacklist, VPN detection and account locking

↑ **Parent:** [News](../news-split.md)  
🏷️ **Tags:** [Account locking](../account-locking.md), [OurBigBook VPN blocking](../ourbigbook-vpn-blocking.md), [OurBigBook Web signup IP blacklist](../ourbigbook-web-signup-ip-blacklist.md), [`-W`, `--web`](../web.md)

As described at: [https://github.com/ourbigbook/ourbigbook/issues/346](https://github.com/ourbigbook/ourbigbook/issues/346), starting December 2024 and increasingly so through January and February 2025, [OurBigBook.com](../ourbigbook-com.md) has been increasingly targeted by a SAPMmer group.

About half of the SPAM posts were advertising cryptocurrency recovery services, but other scammy products were also advertized.

They usually create a few posts every day, but they are very persistent and keep coming back day after day.

The spammers were rather sophisticated:
- almost always one SPAM post per account
- all accounts use gmail addresses, presumably bought in bulk
- the SPAMers use one of a variety of free VPN, most notably ExpressVPN, NordVPN and PIA

At first we were rather amused that there would be human labor so cheap as to make such a work economically feasible.

Adding SPAM to a website that has zero users and almost no views. Amazing!

And it has to be manual work because the website is already protected by [OurBigBook Web reCAPTCHA setup](../ourbigbook-web-recaptcha-setup.md).

Furthermore all of the above strongly indicate a well organized SPAM operation that spams across a variety of websites for a variety of clients.

But what really impressed us the most was [https://ourbigbook.com/alannakennedy/top-ways-to-recover-funds-from-cryptocurrency-scam-iforce-hacker-recovery](https://ourbigbook.com/alannakennedy/top-ways-to-recover-funds-from-cryptocurrency-scam-iforce-hacker-recovery) They actually upvoted a single post from 13 other accounts, making it by far the top article on [OurBigBook.com](../ourbigbook-com.md) as visible at: [https://ourbigbook.com/go/articles?sort=score](https://ourbigbook.com/go/articles?sort=score)

<a id="image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com"></a>
<img src="https://raw.githubusercontent.com/ourbigbook/ourbigbook-media/master/feature/spam/crypto.png" alt="" height="971">

**[Figure 7](#image-screenshot-showing-voting-manipulated-spam-as-the-most-highly-upvoted-article-on-ourbigbook-com). Screenshot showing voting manipulated SPAM as the most highly upvoted article on OurBigBook.com**. [Source](https://web.archive.org/web/20250228110911/https://ourbigbook.com/go/articles?sort=score).

Initially Ciro was debating to himself if he should allow this to continue or not. It is kind of fun to see them work and build a database of compromised gmail addresses.

But finally, Ciro decided to put a stop to it mostly because:
- they create so many accounts that it would take a lot of effort to go over all of them to decide which accounts are legit or not if in the future we wanted to nuke the SPAM accounts
- manipulating the voting system was a step to far

As a result, we have implemented the following features on the website, which should completely kill off this wave of SPAM, while hopefully having little impact to legitimate users:
- [OurBigBook VPN blocking](../ourbigbook-vpn-blocking.md): we now detect and forbid users from signing up from IPs of well known VPNs. The detection is done via API calls to [https://ipapi.is/](https://ipapi.is/) which allows fo 1000 free daily requests. We only make the requests after [reCAPTCHA](../ourbigbook-web-recaptcha-setup.md), and if that service is ever down for some reason, we just skip the check instead
- [OurBigBook Web signup IP blacklist](../ourbigbook-web-signup-ip-blacklist.md): additionally, a small percentage of the SPAM was coming from Pakistani IPs which were not marked as part of a VPN. So we have also given the ability for admins to block some IPs manually to cover those
- [Account locking](../account-locking.md): for SPAM that goes through, we intend to use this new feature to [lock](../account-locking.md) the SPAM accounts, which prevents them from further editing the database in any way, e.g. creating articles

Furthermore, we will also use the pre-existing [unlisted](../ourbigbook-web-unlisted-articles.md) article feature to unlist any particularly noisy spam such as the vote manipulated post.

Announcements:
- [https://mastodon.social/@ourbigbook/114081249345123512](https://mastodon.social/@ourbigbook/114081249345123512)
- [https://x.com/OurBigBook/status/1895434750376165482](https://x.com/OurBigBook/status/1895434750376165482)
- [https://www.linkedin.com/feed/update/urn:li:share:7301200741862420480](https://www.linkedin.com/feed/update/urn:li:share:7301200741862420480)
- [https://www.facebook.com/OurBigBook/posts/pfbid0QPh3kRDe4bA99MpsVNEXX6LqURKooYMjWX3wC6phGrs2vv7PswyTs2GpwX3KTxUCl](https://www.facebook.com/OurBigBook/posts/pfbid0QPh3kRDe4bA99MpsVNEXX6LqURKooYMjWX3wC6phGrs2vv7PswyTs2GpwX3KTxUCl)

## ↑ Ancestors (4)

1. [News](../news-split.md)
2. [Publicity](../publicity.md)
3. [Developing OurBigBook](../developing-ourbigbook.md)
4. [OurBigBook Project](../split.md)
