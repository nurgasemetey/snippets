### execute function after find


[bash - find -exec a shell function in Linux? - Stack Overflow](https://stackoverflow.com/questions/4321456/find-exec-a-shell-function-in-linux "bash - find -exec a shell function in Linux? - Stack Overflow")




```shell
find . | while read file; do dosomething "$file"; done

```
