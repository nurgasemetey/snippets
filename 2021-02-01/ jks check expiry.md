###  jks check expiry


[How to check and monitor SSL certificates expiration with Telegraf - Blog | Songrgg](https://songrgg.github.io/operation/how-to-check-and-monitor-tls-jks-certificates-with-telegraf/ "How to check and monitor SSL certificates expiration with Telegraf - Blog | Songrgg")


 

```
keytool -list -v -keystore your.jks -storepass "pass" | grep until
```
