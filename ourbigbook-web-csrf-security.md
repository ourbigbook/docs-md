# OurBigBook Web CSRF security

↑ **Parent:** [OurBigBook Web architecture](ourbigbook-web-architecture.md)

For a general introduction to CSRF see: [https://security.stackexchange.com/questions/8264/why-is-the-same-origin-policy-so-important/72569#72569](https://security.stackexchange.com/questions/8264/why-is-the-same-origin-policy-so-important/72569#72569)

CSRF security is organized as follows:
- unsafe methods such as POST are all authenticated by JWT. This authentication comes from headers that can only be sent via JavaScript, so it is not possible to make users click links that will take those actions
- safe methods such as GET are authenticated by a cookie. The cookie has the same value as the JWT. It is possible for third party websites to make such authenticated requests, but it doesn't matter as they will not alter the server state, and contents cannot be read back due to the single origin policy.

  There is currently one exception to this: the verification page, which has side effects based on GET. But it shouldn't matter in that specific case.

The JWT token is only given to users after account verification. Having the JWT token is the definition of being logged in.

## ↑ Ancestors (4)

1. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
2. [OurBigBook Web development](ourbigbook-web-development.md)
3. [OurBigBook Web](ourbigbook-web.md)
4. [OurBigBook Project](split.md)
