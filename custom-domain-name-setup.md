# Custom domain name setup

↑ **Parent:** [Heroku deployment](heroku-deployment.md)

The domain [OurBigBook.com](ourbigbook-com.md) was leased from: [https://porkbun.com/](https://porkbun.com/). Unfortunately, HTTPS on Heroku with a custom domain requires using a paying tier, so we upgraded from the free tier to the cheapest paid tier, "Hobby Project", to start with: [https://stackoverflow.com/questions/52185560/heroku-set-ssl-certificates-on-free-plan](https://stackoverflow.com/questions/52185560/heroku-set-ssl-certificates-on-free-plan)

On the Porkbun web UI, we added a DNS record of type :
```
ALIAS ourbigbook.com <heroku-id>.herokudns.com
```
where `heroku-id` was obtained from:
```
heroku domains:add ourbigbook.com
heroku domains
```
and we removed all other `ALIAS`/`CNAME` records from Porkbun.

Next, we setup forwarding from `ciro@ourbigbook.com` to [Ciro Santilli](ciro-santilli.md)'s personal gmail account. This is done in part because it appears that we are required to provide a from address for [OurBigBook Web email sending with Sendgrid](ourbigbook-web-email-sending-with-sendgrid.md), and that email has to be verified. Having Porkbun host it costs 2$/month, and we are trying to use as much free stuff as possible until there are actual users on the website.

Note that if you try to test from your own personal account, the redirect automatically skips sending as it notices that it would redirect to the sender. To test it you have to use some secondary email account instead.

## 🏷️ Tagged (1)

- [OurBigBook.com](ourbigbook-com.md)

## ↑ Ancestors (5)

1. [Heroku deployment](heroku-deployment.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [OurBigBook Web email sending with Sendgrid](ourbigbook-web-email-sending-with-sendgrid.md)
