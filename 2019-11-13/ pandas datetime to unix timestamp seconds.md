###  pandas datetime to unix timestamp seconds

[python - pandas datetime to unix timestamp seconds - Stack Overflow](https://stackoverflow.com/questions/54313463/pandas-datetime-to-unix-timestamp-seconds "python - pandas datetime to unix timestamp seconds - Stack Overflow")




```python
pd.to_datetime(['2019-01-15 13:30:00']).astype(int) / 10**9


##[python - Convert pandas DateTimeIndex to Unix Time? - Stack Overflow](https://stackoverflow.com/questions/15203623/convert-pandas-datetimeindex-to-unix-time "python - Convert pandas DateTimeIndex to Unix Time? - Stack Overflow")
df['<time_col>'].astype(np.int64) // 10**9

```

