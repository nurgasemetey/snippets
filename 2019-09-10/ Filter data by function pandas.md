###  Filter data by function pandas


[python 3.x - Pandas filter data frame rows by function - Stack Overflow](https://stackoverflow.com/questions/51589573/pandas-filter-data-frame-rows-by-function)


 

```python
def filter_fn(row):
    if row['Name'] == 'Alisa' and row['Age'] > 24:
        return False
    else:
        return True

df = pd.DataFrame(d, columns=['Name', 'Age', 'Score'])
m = df.apply(filter_fn, axis=1)
```
