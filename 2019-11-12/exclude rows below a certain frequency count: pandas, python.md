### exclude rows below a certain frequency count: pandas, python


[Python pandas: exclude rows below a certain frequency count - Stack Overflow](https://stackoverflow.com/questions/30485151/python-pandas-exclude-rows-below-a-certain-frequency-count "Python pandas: exclude rows below a certain frequency count - Stack Overflow")


 

```shell
In [136]:
counts = df['positions'].value_counts()
counts

Out[136]:
1    4
3    2
2    1
dtype: int64

In [137]:
counts[counts > 3]

Out[137]:
1    4
dtype: int64

In [135]:
df[df['positions'].isin(counts[counts > 3].index)]

Out[135]:
   r vals  positions
0     1.2          1
2     2.3          1
3     1.8          1
6     1.9          1
```
