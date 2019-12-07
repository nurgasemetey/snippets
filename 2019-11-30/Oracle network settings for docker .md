### Oracle network settings for docker 





 

```shell
sudo iptables -A INPUT -p tcp --destination-port 27017 -m state --state NEW,ESTABLISHED -j ACCEPT 
sudo iptables -A OUTPUT -p tcp --source-port 27017 -m state --state ESTABLISHED -j ACCEPT 

create vcn
create internet gateway 
create route table
```
