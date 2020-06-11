###  string to datetime python


[python - Converting string into datetime - Stack Overflow](https://stackoverflow.com/questions/466345/converting-string-into-datetime "python - Converting string into datetime - Stack Overflow")


 

```
>>> from datetime import datetime

>>> date_string = "2012-12-12 10:10:10"
>>> print (datetime.fromisoformat(date_string))
>>> 2012-12-12 10:10:10
```
