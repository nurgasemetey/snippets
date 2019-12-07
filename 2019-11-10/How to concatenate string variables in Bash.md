### How to concatenate string variables in Bash


[shell - How to concatenate string variables in Bash - Stack Overflow](https://stackoverflow.com/questions/4181703/how-to-concatenate-string-variables-in-bash "shell - How to concatenate string variables in Bash - Stack Overflow")


 

```shell
a='Hello'
b='World'
c="${a} ${b}"
echo "${c}"
> Hello World
```
