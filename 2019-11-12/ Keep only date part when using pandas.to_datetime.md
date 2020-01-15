###  Keep only date part when using pandas.to_datetime


[python - Keep only date part when using pandas.to_datetime - Stack Overflow](https://stackoverflow.com/questions/16176996/keep-only-date-part-when-using-pandas-to-datetime "python - Keep only date part when using pandas.to_datetime - Stack Overflow")

[pandas.Series.dt.date — pandas 0.25.3 documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.date.html "pandas.Series.dt.date — pandas 0.25.3 documentation")


```python
df['date_only'] = df['date_time_column'].dt.date
df_final["hour"]= df_final["ts2"].dt.hour
```
