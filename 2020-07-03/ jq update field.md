###  jq update field


[How do I update a single value in a json document using jq? - Stack Overflow](https://stackoverflow.com/questions/31034746/how-do-i-update-a-single-value-in-a-json-document-using-jq "How do I update a single value in a json document using jq? - Stack Overflow")


 

```bash
jq --arg text "$text" '."custom-label".value = $text' $articlePath
```
