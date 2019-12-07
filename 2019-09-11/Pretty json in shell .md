### Pretty json in shell 


[unix - How can I pretty-print JSON in a shell script? - Stack Overflow](https://stackoverflow.com/questions/352098/how-can-i-pretty-print-json-in-a-shell-script)




```shell
$ jq . <<< '{ "foo": "lorem", "bar": "ipsum" }'
{
  "bar": "ipsum",
  "foo": "lorem"
}
```

