###  regex file python


[10.8. fnmatch — Unix filename pattern matching — Python 2.7.18 documentation](https://docs.python.org/2/library/fnmatch.html "10.8. fnmatch — Unix filename pattern matching — Python 2.7.18 documentation")


 

```python
intervals = ["08:00:00", "08:30:00", "09:00:00", "09:30:00"]
for interval in intervals:
    gps_occurence_map = {}
    for file in os.listdir('json_files'):
        if fnmatch.fnmatch(file, f'*{interval}*'):
```
