# OurBigBook VPN blocking

↑ **Parent:** [OurBigBook Web deployment](ourbigbook-web-deployment.md)

[OurBigBook Web](ourbigbook-web.md) supports blocking VPN users from signing up in order to reduce SPAM.

This is currently done by making API calls to [https://ipapi.is/](https://ipapi.is/) after the [reCAPTCHA](ourbigbook-web-recaptcha-setup.md) check.

To enable this, you must set the `OURBIGBOOK_IPAPI_IS_API_KEY` environment variable to contain your API key, which can be obtained by signing up to the freemium service:
```
./heroku config:set OURBIGBOOK_IPAPI_IS_API_KEY=api_key
```
To test locally, the checks ca be enabled with:
```
OURBIGBOOK_IPAPI_IS_API_KEY=api_key OURBIGBOOK_DEV_IP=123.456.789.1 npm run dev
```
which also fakes an IP with [`OURBIGBOOK_DEV_IP`](ourbigbook-dev-ip.md).

## 🏷️ Tagged (1)

- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)

## ↑ Ancestors (4)

1. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)

## ← Incoming links (3)

- [Heroku deployment](heroku-deployment.md)
- [Signup IP blacklist, VPN detection and account locking](news/signup-ip-blacklist-vpn-detection-and-account-locking.md)
- [OurBigBook Web environment variable](ourbigbook-web-environment-variable.md)
