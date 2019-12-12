###  Requests vs Limits in Kubernetes


[Requests vs Limits in Kubernetes – Vincent-Philippe Lauzon's](https://vincentlauzon.com/2019/04/02/requests-vs-limits-in-kubernetes/ "Requests vs Limits in Kubernetes – Vincent-Philippe Lauzon's")


 

```
Requests	
The requests specification is used at pod placement time: Kubernetes will look for a node that has both enough CPU and memory according to the requests configuration.
Limits	
This is enforced at runtime. If a container exceeds the limits, Kubernetes will try to stop it. For CPU, it will simply curb the usage so a container typically can’t exceed its limit capacity ; it won’t be killed, just won’t be able to use more CPU. If a container exceeds its memory limits, it could be terminated.
```
