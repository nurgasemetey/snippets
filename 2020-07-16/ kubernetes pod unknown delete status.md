###  kubernetes pod unknown delete status


[Container pods stuck ins tate unknown · Issue #43279 · kubernetes/kubernetes](https://github.com/kubernetes/kubernetes/issues/43279 "Container pods stuck ins tate unknown · Issue #43279 · kubernetes/kubernetes")


 

```
kubectl delete pods <unknown pods name> --grace-period=0 --force
kubectl delete pods --all  --grace-period=0 --force
```
