### Passing bash variable to jq select


[json - Passing bash variable to jq select - Stack Overflow](https://stackoverflow.com/questions/40027395/passing-bash-variable-to-jq-select)


 

```shell
projectID=$(cat file.json | jq -r ".resource[] | select(.username==\"$EMAILID\") | .id")

```
