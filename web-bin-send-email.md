<h1 id="web-bin-send-email">web/bin/send-email</h1>

↑ **Parent:** [OurBigBook Web email sending](ourbigbook-web-email-sending.md)  
🏷️ **Tags:** [Web CLI utils](web-cli-utils.md)

This utilit serves as a quick test to check if email sending is working, without you having to click a bunch of buttons on the web UI such as creating a new user:
```
cd web
OURBIGBOOK_SEND_EMAIL=ses \
    OURBIGBOOK_SEND_EMAIL_SES_REGION=us-east-1 \
    OURBIGBOOK_SEND_EMAIL_SES_USERNAME=access-key \
    OURBIGBOOK_SEND_EMAIL_SES_API_KEY=secret-access-key \
    bin/send-email user@mail.com 'My subject' 'My body'
```

## ↑ Ancestors (5)

1. [OurBigBook Web email sending](ourbigbook-web-email-sending.md)
2. [OurBigBook Web deployment](ourbigbook-web-deployment.md)
3. [OurBigBook Web development](ourbigbook-web-development.md)
4. [OurBigBook Web](ourbigbook-web.md)
5. [OurBigBook Project](split.md)
