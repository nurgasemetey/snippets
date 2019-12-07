### Access to VM from pods






 

```shell
gcloud compute firewall-rules create "test-metis-to-all-vms-on-network" --network="default" --source-ranges="10.16.0.0/14" --allow=tcp,udp,icmp,esp,ah,sctp
```
