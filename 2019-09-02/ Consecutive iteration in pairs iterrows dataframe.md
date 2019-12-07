###  Consecutive iteration in pairs iterrows dataframe


[python - Pandas iterate over DataFrame row pairs - Stack Overflow](https://stackoverflow.com/questions/51443725/pandas-iterate-over-dataframe-row-pairs)


 

```python
df_merged = pd.concat([df, df.shift(-1).add_prefix('next_')], axis=1)
df_merged
#Out:
   a  b interval     next_a     next_b    next_interval
0  1  2   [1, 3]        3.0        4.0           [2, 4]
1  3  4   [2, 4]        5.0        6.0           [6, 9]
2  5  6   [6, 9]        7.0        8.0          [9, 10]
3  7  8  [9, 10]        NaN        NaN              NaN
```
