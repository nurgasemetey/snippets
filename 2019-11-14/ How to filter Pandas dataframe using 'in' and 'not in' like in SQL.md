###  How to filter Pandas dataframe using 'in' and 'not in' like in SQL


[python - How to filter Pandas dataframe using 'in' and 'not in' like in SQL - Stack Overflow](https://stackoverflow.com/questions/19960077/how-to-filter-pandas-dataframe-using-in-and-not-in-like-in-sql "python - How to filter Pandas dataframe using 'in' and 'not in' like in SQL - Stack Overflow")


 

```python
You can use pd.Series.isin.

For "IN" use: something.isin(somewhere)

Or for "NOT IN": ~something.isin(somewhere)
```
