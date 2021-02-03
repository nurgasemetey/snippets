###  check expiry p12


[How to check and monitor SSL certificates expiration with Telegraf - Blog | Songrgg](https://songrgg.github.io/operation/how-to-check-and-monitor-tls-jks-certificates-with-telegraf/ "How to check and monitor SSL certificates expiration with Telegraf - Blog | Songrgg")


 

```
openssl pkcs12 -in certicate.p12 -nokeys | openssl x509 -noout -enddate
```
