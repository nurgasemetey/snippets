###  Complex filter on rows dataframe pandas


[python - pandas: complex filter on rows of DataFrame - Stack Overflow](https://stackoverflow.com/questions/11418192/pandas-complex-filter-on-rows-of-dataframe)


 

```python
In [3]: df = pandas.DataFrame(np.random.randn(5, 3), columns=['a', 'b', 'c'])

In [4]: df
Out[4]: 
          a         b         c
0 -0.001968 -1.877945 -1.515674
1 -0.540628  0.793913 -0.983315
2 -1.313574  1.946410  0.826350
3  0.015763 -0.267860 -2.228350
4  0.563111  1.195459  0.343168

In [6]: df[df.apply(lambda x: x['b'] > x['c'], axis=1)]
Out[6]: 
          a         b         c
1 -0.540628  0.793913 -0.983315
2 -1.313574  1.946410  0.826350
3  0.015763 -0.267860 -2.228350
4  0.563111  1.195459  0.343168
```
