# OurBigBook Web email sending with AWS SES

↑ **Parent:** [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)

This is the current method used on [OurBigBook.com](ourbigbook-com.md). They currenly offer pay as you go mailing at 1$ / 10,000 emails sent, which feels reasonable.

```
OURBIGBOOK_SEND_EMAIL=ses \
    OURBIGBOOK_SEND_EMAIL_SES_REGION=us-east-1 \
    OURBIGBOOK_SEND_EMAIL_SES_USERNAME=access-key \
    OURBIGBOOK_SEND_EMAIL_SES_API_KEY=secret-access-key \
    npm run dev
```

The initial setup is slightly annoying as you have to write to support for them to enable your account, much like other AWS products, but once that is done we managed to get it working fine.

Announced at: 
- [https://mastodon.social/@ourbigbook/114970958914849281](https://mastodon.social/@ourbigbook/114970958914849281)
- [https://x.com/OurBigBook/status/1952376470849859661](https://x.com/OurBigBook/status/1952376470849859661)
- [https://www.linkedin.com/feed/update/urn:li:share:7358142308652838912](https://www.linkedin.com/feed/update/urn:li:share:7358142308652838912)
- [https://www.facebook.com/OurBigBook/posts/pfbid034bsRDjfp6aRsG8EwBQnBxBrm5yPe9uaEWeHHJoyVUjEzJDTAREyApcNPzMhBpSkGl](https://www.facebook.com/OurBigBook/posts/pfbid034bsRDjfp6aRsG8EwBQnBxBrm5yPe9uaEWeHHJoyVUjEzJDTAREyApcNPzMhBpSkGl)

## ↑ Ancestors (6)

1. [OurBigBook Web email sending with](ourbigbook-web-email-sending-with.md)
2. [OurBigBook Web email sending](ourbigbook-web-email-sending.md)
3. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
4. [OurBigBook Web development](ourbigbook-web-development.md)
5. [OurBigBook Web](ourbigbook-web.md)
6. [OurBigBook Project](split.md)
