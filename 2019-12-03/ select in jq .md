###  select in jq 





 

```shell
jq '.elements | .[] | select(.type=="way") | .type' secondary.json |wc
```
