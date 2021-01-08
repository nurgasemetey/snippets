### parsing time string in Python


[datetime - Parsing time string in Python - Stack Overflow](https://stackoverflow.com/questions/10494312/parsing-time-string-in-python "datetime - Parsing time string in Python - Stack Overflow")


 

```python
>>> from datetime import datetime
>>> date_str = 'Tue May 08 15:14:45 +0800 2012'
>>> date = datetime.strptime(date_str, '%a %B %d %H:%M:%S +0800 %Y')
>>> date
datetime.datetime(2012, 5, 8, 15, 14, 45)
```
