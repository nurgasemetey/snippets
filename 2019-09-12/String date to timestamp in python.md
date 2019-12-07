### String date to timestamp in python


[datetime - Convert string date to timestamp in Python - Stack Overflow](https://stackoverflow.com/questions/9637838/convert-string-date-to-timestamp-in-python)




```python
import datetime
stime = "01/12/2011"
print(datetime.datetime.strptime(stime, "%d/%m/%Y").timestamp())
##To use UTC instead of the local timezone use .replace:
datetime.datetime.strptime(stime, "%d/%m/%Y").replace(tzinfo=datetime.timezone.utc).timestamp()

```
