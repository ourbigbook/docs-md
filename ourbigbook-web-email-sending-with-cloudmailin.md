# OurBigBook Web email sending with cloudmailin

↑ **Parent:** [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)

We set them up as a Heroku plugin, and the login into cloudmailin is done through Heroku.

Username and API keys are the same as the SMTP values.

You need to setup a domain to take the account out of test mode.

After a day they sent an email saying the DNS entries that neede to be changed:
```
mta.ourbigbook.com CNAME feedback-smtp.cloudmta.net
e210040093cm.ourbigbook.com	TXT long-thing-in-attachment
```

But TODO even after that it still failed with:
```
Domain has already been taken
Mta domain has already been taken
```
when we input `ourbigbook.com`.

## ↑ Ancestors (6)

1. [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)
2. [OurBigBook Web email sending](ourbigbook-web-email-sending.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)
