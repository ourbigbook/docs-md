# OurBigBook Web email sending with Sendgrid

↑ **Parent:** [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)

- ensure that you have a working email address in the hosted domain such as `notification@ourbigbook.com`. E.g. on our [custom domain name setup](custom-domain-name-setup.md) with Porkbun. We achieved this by redirecting `notification@ourbigbook.com` to your personal email initially.
- create a Sendgrid account
  - it would also be a good idea to setup two factor authentication
- verify your domain, e.g. `ourbigbook.com`. This means setting up three `CNAME` records given by Sendgrid on your DNS provider, e.g. Porkbun.
- create a single sender. We used:
  - From Name: OurBigBook.com
  - From Email Address: `notification@ourbigbook.com`
  - Reply to: `notification@ourbigbook.com`
- we disabled their "link tracking" feature, which was turned on by default. While it is fun to track clicks, it is basically useless for transactional email, and it parse HTML and replaces the links with their tracking links, making things less clear for end users. It is also harder to debug.
- integrate using web API
  - create an API key, and then save it on Heroku:
    ```
    heroku config:set -a ourbigbook OURBIGBOOK_SEND_EMAIL_SENDGRID_API_KEY=thekey
    ```

    Also set it locally to be able to test email sending integration locally:
    ```
    echo ourbigbook OURBIGBOOK_SEND_EMAIL_SENDGRID_API_KEY=thekey >> web/.env
    ```

    Then, to verify that the email sending is actually working run;
    ```
    env $(cat .env | xargs) OURBIGBOOK_SEND_EMAIL=cloudmailin npm run dev
    ```

    and try to register some of your real emails. You should actually receive the email at this step. The email appears as sent from:
    ```
    ciro@ourbigbook.com via sendgrid.net
    ```

    gmail accepted the email under promotions without domain verification, but outlook sent it to spam. Make sure to click "it is not spam" in that case.

## ↑ Ancestors (6)

1. [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)
2. [OurBigBook Web email sending](ourbigbook-web-email-sending.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)

## ← Incoming links (2)

- [Custom domain name setup](custom-domain-name-setup.md)
- [Heroku deployment](heroku-deployment.md)
