### character replace pandas dataframe python


[Python Pandas: How to replace a characters in a column of a dataframe? - Stack Overflow](https://stackoverflow.com/questions/28986489/python-pandas-how-to-replace-a-characters-in-a-column-of-a-dataframe)




```python
df['range'] = df['range'].str.replace(',','-')

```
