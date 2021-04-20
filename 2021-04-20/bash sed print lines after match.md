### bash sed print lines after match


[regex - Sed : print all lines after match - Stack Overflow](https://stackoverflow.com/questions/32569032/sed-print-all-lines-after-match "regex - Sed : print all lines after match - Stack Overflow")


 

```
$ sed -ne '/pattern/,$ p'
  # alternatively, if you don't want to print the match:
$ sed -e '1,/pattern/ d'
```
