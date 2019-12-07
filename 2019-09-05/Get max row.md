### Get max row


[python - Pandas max value index - Stack Overflow](https://stackoverflow.com/questions/39964558/pandas-max-value-index)




```python
df.loc[df['favcount'].idxmax(), 'sn']
```
