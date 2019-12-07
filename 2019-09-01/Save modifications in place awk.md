### Save modifications in place awk


[linux - Save modifications in place with awk - Stack Overflow](https://stackoverflow.com/questions/16529716/save-modifications-in-place-with-awk)


Unless you have GNU awk 4.1.0 or later...

You won't have such an option as sed's -i option so instead do:

```shell
awk '{print $0}' file > tmp && mv tmp file

```
