### Scaling in kubernetes 


[Scaling an application | Kubernetes Engine Documentation | Google Cloud](https://cloud.google.com/kubernetes-engine/docs/how-to/scaling-apps "Scaling an application  |  Kubernetes Engine Documentation  |  Google Cloud")


 

```shell
kubectl autoscale deployment my-app --max 6 --min 4 --cpu-percent 50
```
