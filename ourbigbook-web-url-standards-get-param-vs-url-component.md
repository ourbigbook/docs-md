# OurBigBook Web URL standards: GET param vs url component

↑ **Parent:** [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)

Next.js imposes one constraint: ISR only works with URL parameters like `/articles/<page>`, not GET parameters like `/articles?page=1`.

As of writing however, we don't use any ISR as it adds a lot of complication. But still, we are trying to stick to the general principle that if something might ever be ISR'ed in the future, then we would like to keep it as parameter rather then GET. It feels sane.

The only things that we are ever consider ISR'ing are the pre-rendered version of articles and issues, excluding any metadata of those that changes often or depends on logged in users.

All lists of things will never be ISR'ed, as those can change constantly. One conclusion of this is that:
- page number
- ordering
- other search-like parameters
which appear only in lists of things, will always be part of the GET query, and not params.

Types:
- booleans are:
  - `0` for false
  - `1` for true
- tristate booleans are:
  - `0` for false
  - `1` for true
  - `2` for all

  These are used for example when filtering booleans where the default is to show only either true or false but not both, e.g., we hide locked users by default, i.e. `locked=0` is the default, therefore we have:
  - [http://localhost:3000/go/users?locked=0](http://localhost:3000/go/users?locked=0): show only unlocked users. Same as the default [http://localhost:3000/go/users](http://localhost:3000/go/users).
  - [http://localhost:3000/go/users?locked=1](http://localhost:3000/go/users?locked=1): show only locked users.
  - [http://localhost:3000/go/users?locked=2](http://localhost:3000/go/users?locked=2): show both locked and unlocked users.

  The user list also hides users without verified email by default:
  - [http://localhost:3000/go/users?verified=1](http://localhost:3000/go/users?verified=1): show only users with verified email. Same as the default [http://localhost:3000/go/users](http://localhost:3000/go/users).
  - [http://localhost:3000/go/users?verified=0](http://localhost:3000/go/users?verified=0): show only users with unverified email.
  - [http://localhost:3000/go/users?verified=2](http://localhost:3000/go/users?verified=2): show users with both verified and unverified email.

## ↑ Ancestors (5)

1. [OurBigBook Web URL standards](ourbigbook-web-url-standards.md)
2. [OurBigBook Web architecture](ourbigbook-web-architecture.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
