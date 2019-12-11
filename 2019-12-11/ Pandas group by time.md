###  Pandas group by time


[python - pandas grouper vs time grouper - Stack Overflow](https://stackoverflow.com/questions/47015886/pandas-grouper-vs-time-grouper "python - pandas grouper vs time grouper - Stack Overflow")


 

```python
df['column_name'] = pd.to_datetime(df['column_name'])
# new version
df.groupby(pd.Grouper(key='column_name', freq="M")).mean().plot()
```
