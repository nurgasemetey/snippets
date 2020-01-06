### Remove first line in bash


[scripting - How can I remove the first line of a text file using bash/sed script? - Stack Overflow](https://stackoverflow.com/questions/339483/how-can-i-remove-the-first-line-of-a-text-file-using-bash-sed-script#comment55780681_27099557 "scripting - How can I remove the first line of a text file using bash/sed script? - Stack Overflow")




```shell
tail -n +2 "$temp_file" > $without_header_temp_file
```
