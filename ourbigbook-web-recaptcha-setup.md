# OurBigBook Web reCAPTCHA setup

↑ **Parent:** [OurBigBook Web deployment](ourbigbook-web-deployment.md)

Go to [https://www.google.com/recaptcha/about/](https://www.google.com/recaptcha/about/), setup a new domain, and save the values given e.g. to Heroku for [Heroku deployment](heroku-deployment.md):
```
./heroku config:set RECAPTCHA_SECRET_KEY=secret_key
./heroku config:set NEXT_PUBLIC_RECAPTCHA_SITE_KEY=site_key
```

Aditionally, also setup a separate localhost reCAPTCHA to test that it is working:
```
echo RECAPTCHA_SECRET_KEY=secret_localhost_key >> web/.env
echo NEXT_PUBLIC_RECAPTCHA_SITE_KEY=site_localhost_key >> web/.env
```
and then to use the .env file run with:
```
cd web
env $(cat .env | xargs) npm run dev
```

Although it is possible to use a single reCAPTCHA for both production and development, Google recommends having separate ones.

If the `NEXT_PUBLIC_RECAPTCHA_SITE_KEY` variable is not set, then reCAPTCHA is simply not used in the website.

## ↑ Ancestors (4)

1. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Heroku deployment](heroku-deployment.md)
- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)
- [OurBigBook VPN blocking](ourbigbook-vpn-blocking.md)
