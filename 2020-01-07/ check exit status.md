###  check exit status


[bash - How to check the exit status using an if statement - Stack Overflow](https://stackoverflow.com/questions/26675681/how-to-check-the-exit-status-using-an-if-statement "bash - How to check the exit status using an if statement - Stack Overflow")


 

```shell
exit_status=$?
if [ $exit_status -eq 1 ]; then
    echo "blah blah blah"
fi
exit $exit_status
```
