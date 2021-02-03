### check expiry crt file openssl


[How To Check SSL Certificate Expiration with OpenSSL | ComputingForGeeks](https://computingforgeeks.com/how-to-check-ssl-certificate-expiration-with-openssl/#:~:text=crt%20should%20be%20replaced%20with%20the%20correct%20path%20to%20your%20crt%20file.&text=The%20expiration%20date%20for%20certificate,23%3A59%3A59%202020. "How To Check SSL Certificate Expiration with OpenSSL | ComputingForGeeks")


 

```
$ cat /etc/kubernetes/kubelet-ca.crt | openssl x509 -noout -enddate
notAfter=Aug  5 21:38:23 2029 GMT
```
