###  jq replace update field file


[bash - Jq to replace text directly on file (like sed -i) - Stack Overflow](https://stackoverflow.com/questions/36565295/jq-to-replace-text-directly-on-file-like-sed-i "bash - Jq to replace text directly on file (like sed -i) - Stack Overflow")


 

```bash
jq --arg text "$text" '."custom-label".value = $text' $articlePath| sponge $articlePath
```
