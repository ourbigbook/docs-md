# OurBigBook Web email sending

↑ **Parent:** [OurBigBook Web deployment](ourbigbook-web-deployment.md)

To send emails, you have to set the environment variable `OURBIGBOOK_SEND_EMAIL` to select which provider you want to use:
```
OURBIGBOOK_SEND_EMAIL=cloudmailin
```
and then use provider specific variables for each provider documented under [Section "OurBigBook Web email sending with"](ourbigbook-web-email-sending-with.md).

This setup can be used to test the email integration locally.

Some research of different methods is shown at: [https://cirosantilli.com/send-free-emails-from-heroku](https://cirosantilli.com/send-free-emails-from-heroku)

Related configurations:
- after reports that useres had received a "Suspicions link" when clicking the signup link on Gmail, we've tried to follow
  - [https://stackoverflow.com/questions/63716879/how-to-prevent-suspicious-link-message-in-gmail/63716961#63716961](https://stackoverflow.com/questions/63716879/how-to-prevent-suspicious-link-message-in-gmail/63716961#63716961)
  - [https://support.google.com/mail/thread/4242603?hl=en&msgid=8208054](https://support.google.com/mail/thread/4242603?hl=en&msgid=8208054)
  - [https://postmaster.google.com/](https://postmaster.google.com/)

  and add a TXT record of:
  ```
  google-site-verification=gctCPztssfR8A-fQ_5298gSee_DfFjBj8v9PqAxuhgU
  ```

  to the domain, which Google marked as verified. Let's see if helps.

**Table of contents**

- [web/bin/send-email](web-bin-send-email.md)
- [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)
  - [OurBigBook Web email sending with AWS SES](ourbigbook-web-email-sending-with-aws-ses.md)
  - [OurBigBook Web email sending with cloudmailin](ourbigbook-web-email-sending-with-cloudmailin.md)
  - [OurBigBook Web email sending with Sendgrid](ourbigbook-web-email-sending-with-sendgrid.md)

## ↑ Ancestors (4)

1. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (1)

- [Heroku deployment](heroku-deployment.md)
