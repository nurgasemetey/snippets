### Creating an empty Pandas DataFrame


[python - Creating an empty Pandas DataFrame, then filling it? - Stack Overflow](https://stackoverflow.com/questions/13784192/creating-an-empty-pandas-dataframe-then-filling-it)


 

```python
If you want to have your column names in place from the start, use this approach:

import pandas as pd

col_names =  ['A', 'B', 'C']
my_df  = pd.DataFrame(columns = col_names)
my_df
If you want to add a record to the dataframe it would be better to use:

my_df.loc[len(my_df)] = [2, 4, 5]
You also might want to pass a dictionary:

my_dic = {'A':2, 'B':4, 'C':5}
my_df.loc[len(my_df)] = my_dic 
However if you want to add another dataframe to my_df do as follows:

col_names =  ['A', 'B', 'C']
my_df2  = pd.DataFrame(columns = col_names)
my_df = my_df.append(my_df2)
If you are adding rows inside a loop consider performance issues:
For around the first 1000 records "my_df.loc" performance is better, but it gradually becomes slower by increasing the number of records in the loop.

If you plan to do thins inside a big loop (say 10M‌ records or so):
You are better off using a mixture of these two; fill a dataframe with iloc until the size gets around 1000, then append it to the original dataframe, and empty the temp dataframe. This would boost your performance by around 10 times.
```
