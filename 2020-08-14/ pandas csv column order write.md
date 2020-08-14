###  pandas csv column order write


[Preserving column order in Python Pandas DataFrame - Stack Overflow](https://stackoverflow.com/questions/15653688/preserving-column-order-in-python-pandas-dataframe "Preserving column order in Python Pandas DataFrame - Stack Overflow")


 

```
data = pd.read_csv(filename)
data.to_csv(filename, columns=['a', 'b', 'c', 'd'])

import pandas as pd
data = pd.read_csv(filename)
data2 = df[['A','B','C']]  #put 'A' 'B' 'C' in the desired order
data2.to_csv(filename)

```
