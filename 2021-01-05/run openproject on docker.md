### run openproject on docker





 

```
docker run -d -p 34000:80 --name openproject -e SECRET_KEY_BASE=secret -e EMAIL_DELIVERY_METHOD="smtp" -e SMTP_ADDRESS="smtp.yandex.com" -e SMTP_PORT="465" -e SMTP_DOMAIN="domain" -e SMTP_AUTHENTICATION="login" -e SMTP_USER_NAME="username@domain.com" -e SMTP_PASSWORD="password" -e SMTP_ENABLE_STARTTLS_AUTO="true" -v /var/lib/openproject/pgdata:/var/openproject/pgdata -v /var/lib/openproject/static:/var/openproject/assets --restart always openproject/community:8
```
