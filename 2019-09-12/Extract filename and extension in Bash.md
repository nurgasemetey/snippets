### Extract filename and extension in Bash


[string - Extract filename and extension in Bash - Stack Overflow](https://stackoverflow.com/questions/965053/extract-filename-and-extension-in-bash)


 

```shell
file="thisfile.txt"
echo "filename: ${file%.*}"
echo "extension: ${file##*.}"
```
