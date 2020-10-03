###  pandas loop over groups


[python - Looping over groups in a grouped dataframe - Stack Overflow](https://stackoverflow.com/questions/45797633/looping-over-groups-in-a-grouped-dataframe "python - Looping over groups in a grouped dataframe - Stack Overflow")


 

```
groups = frame.groupby(level=0)

for n,g in groups:
    print('This is group '+ str(n)+'.')
    print(g)
    print('\n')
    for i, row in g.iterrows():
        print(row)
```
