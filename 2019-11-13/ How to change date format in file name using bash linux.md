###  How to change date format in file name using bash/linux


[How to change date format in file name using bash/linux? - Super User](https://superuser.com/questions/1115717/how-to-change-date-format-in-file-name-using-bash-linux "How to change date format in file name using bash/linux? - Super User")




```shell
rename 's/([0-9]{2})-([0-9]{2})-([0-9]{4})/$3-$2-$1/' *
```

