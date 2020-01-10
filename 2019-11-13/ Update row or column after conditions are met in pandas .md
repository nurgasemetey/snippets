###  Update row or column after conditions are met in pandas 

[python - Update row values where certain condition is met in pandas - Stack Overflow](https://stackoverflow.com/questions/36909977/update-row-values-where-certain-condition-is-met-in-pandas "python - Update row values where certain condition is met in pandas - Stack Overflow")

[python - pandas : update value if condition in 3 columns are met - Stack Overflow](https://stackoverflow.com/questions/21263020/pandas-update-value-if-condition-in-3-columns-are-met "python - pandas : update value if condition in 3 columns are met - Stack Overflow")


```python
df1.loc[df1['stream'] == 2, ['feat','another_feat']] = 'aaaa'
print df1
   stream        feat another_feat
a       1  some_value   some_value
b       2        aaaa         aaaa
c       2        aaaa         aaaa
d       3  some_value   some_value

df_final_avg.loc[ (df_final_avg["congestion"] >= 0.84 ) & (df_final_avg["congestion"] < 0.91 ),'congestion_score'] = 2

```

