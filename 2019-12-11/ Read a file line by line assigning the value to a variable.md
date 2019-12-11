###  Read a file line by line assigning the value to a variable


[bash - Read a file line by line assigning the value to a variable - Stack Overflow](https://stackoverflow.com/questions/10929453/read-a-file-line-by-line-assigning-the-value-to-a-variable "bash - Read a file line by line assigning the value to a variable - Stack Overflow")


 

```shell
while IFS= read -r line; do
    echo "Text read from file: $line"
done < my_filename.txt
```
