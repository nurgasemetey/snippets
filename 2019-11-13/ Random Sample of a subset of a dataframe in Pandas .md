###  Random Sample of a subset of a dataframe in Pandas 


[python - Random Sample of a subset of a dataframe in Pandas - Stack Overflow](https://stackoverflow.com/questions/38085547/random-sample-of-a-subset-of-a-dataframe-in-pandas "python - Random Sample of a subset of a dataframe in Pandas - Stack Overflow")


 

```python
In [11]: df = pd.DataFrame([[1, 2], [3, 4], [5, 6], [7, 8]], columns=["A", "B"])

In [12]: df.sample(2)
Out[12]:
   A  B
0  1  2
2  5  6

In [13]: df.sample(2)
Out[13]:
   A  B
3  7  8
0  1  2
```
