###  Convert a timedelta to days, hours and minutes


[python - Convert a timedelta to days, hours and minutes - Stack Overflow](https://stackoverflow.com/questions/2119472/convert-a-timedelta-to-days-hours-and-minutes)


 

```python
days, hours, minutes = td.days, td.seconds // 3600, td.seconds // 60 % 60
```
