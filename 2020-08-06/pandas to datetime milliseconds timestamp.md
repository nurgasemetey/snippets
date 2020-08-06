### pandas to datetime milliseconds timestamp


[python - Pandas converting row with unix timestamp (in milliseconds) to datetime - Stack Overflow](https://stackoverflow.com/questions/34883101/pandas-converting-row-with-unix-timestamp-in-milliseconds-to-datetime "python - Pandas converting row with unix timestamp (in milliseconds) to datetime - Stack Overflow")




```
df['UNIXTIME'] = pd.to_datetime(df['UNIXTIME'], unit='ms')

```
