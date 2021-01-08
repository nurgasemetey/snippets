### delete first N characters bash


[bash - What is a unix command for deleting the first N characters of a line? - Stack Overflow](https://stackoverflow.com/questions/971879/what-is-a-unix-command-for-deleting-the-first-n-characters-of-a-line)


 

```shell
tail -f logfile | grep org.springframework | cut -c 5-
```
