###  jq length array list


[Bash JSON Get Length of Array - Stack Overflow](https://stackoverflow.com/questions/44289743/bash-json-get-length-of-array "Bash JSON Get Length of Array - Stack Overflow")


 

```bash
jq ".[] | .surfaceGeometry[] | .length" roadform-modified.json
```
