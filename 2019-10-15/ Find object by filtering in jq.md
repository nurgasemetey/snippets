###  Find object by filtering in jq


[json - Select objects based on value of variable in object using jq - Stack Overflow](https://stackoverflow.com/questions/18592173/select-objects-based-on-value-of-variable-in-object-using-jq)


 

```shell
jq '.[] | select(.location=="Stockholm") | .name' json
```
