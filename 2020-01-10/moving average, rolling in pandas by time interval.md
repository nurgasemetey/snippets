### moving average, rolling in pandas by time interval


[python - Pandas: rolling mean by time interval - Stack Overflow](https://stackoverflow.com/questions/15771472/pandas-rolling-mean-by-time-interval "python - Pandas: rolling mean by time interval - Stack Overflow")




```python
test_sorted['speed_ma'] = test_sorted["speed_kph"].rolling('1H', min_periods=1).mean()
```
