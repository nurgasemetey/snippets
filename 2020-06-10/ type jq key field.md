###  type jq key field


[json - How to get root keys and key types using jq - Stack Overflow](https://stackoverflow.com/questions/41301988/how-to-get-root-keys-and-key-types-using-jq "json - How to get root keys and key types using jq - Stack Overflow")
[bash - Check JSON data type using jq - Stack Overflow](https://stackoverflow.com/questions/54191177/check-json-data-type-using-jq "bash - Check JSON data type using jq - Stack Overflow")

 

```bash
jq ".[] | .avgSlope | type" roadform-modified.json | sort |uniq

```
