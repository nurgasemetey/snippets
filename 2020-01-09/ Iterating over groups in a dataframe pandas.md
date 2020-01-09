###  Iterating over groups in a dataframe pandas


[python - Iterating over groups in a dataframe - Stack Overflow](https://stackoverflow.com/questions/46230895/iterating-over-groups-in-a-dataframe?noredirect=1&lq=1 "python - Iterating over groups in a dataframe - Stack Overflow")


 

```python
groups = frame.groupby(level=0)

for n,g in groups:
    print('This is group '+ str(n)+'.')
    print(g)
    print('\n')
    for i, row in g.iterrows():
        print(row)
```
