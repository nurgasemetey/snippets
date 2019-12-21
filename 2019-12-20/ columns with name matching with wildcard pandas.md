###  columns with name matching with wildcard pandas


[pandas - Select columns with name matching str with wildcard for t-test (Python) - Stack Overflow](https://stackoverflow.com/questions/46900364/select-columns-with-name-matching-str-with-wildcard-for-t-test-python)




```python
import pandas as pd
df = pd.DataFrame(columns=["a1a","a2a","a1b"])

mask = df.columns.str.contains('a.*a')

df.loc[:,mask] # selects mask
df.loc[:,~mask] # selects inverted (by using ~) mask

###series
row.loc[mask]
```
