###  How to refer to one environment variable from another


[Kubernetes: How to refer to one environment variable from another? - Stack Overflow](https://stackoverflow.com/questions/49582349/kubernetes-how-to-refer-to-one-environment-variable-from-another "Kubernetes: How to refer to one environment variable from another? - Stack Overflow")


 

```shell
containers:
- env:
  - name: POD_ID
    valueFrom: # etc etc
  - name: LOG_PATH
    value: /var/log/mycompany/$(POD_ID)/logs
```
