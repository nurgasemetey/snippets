### Run openproject on docker







```shell
docker run -d -p 8080:80 --name openproject -e SECRET_KEY_BASE=secret -e EMAIL_DELIVERY_METHOD="smtp" -e SMTP_ADDRESS="smtp.yandex.com" -e SMTP_PORT="465" -e SMTP_DOMAIN="paraboly.com" -e  SMTP_AUTHENTICATION="login" -e  SMTP_USER_NAME="info@paraboly.com" -e SMTP_PASSWORD="parabol1" -e SMTP_ENABLE_STARTTLS_AUTO="true"  -v /var/lib/openproject/pgdata:/var/openproject/pgdata   -v /var/lib/openproject/static:/var/openproject/assets   openproject/community:8
```
