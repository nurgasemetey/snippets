###  Keep only date part when using pandas.to_datetime


[python - Keep only date part when using pandas.to_datetime - Stack Overflow](https://stackoverflow.com/questions/16176996/keep-only-date-part-when-using-pandas-to-datetime "python - Keep only date part when using pandas.to_datetime - Stack Overflow")


 

```python
df['date_only'] = df['date_time_column'].dt.date

```
