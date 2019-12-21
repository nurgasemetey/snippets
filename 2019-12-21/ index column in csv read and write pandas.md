###  index column in csv read and write pandas


[python - Removing index column in pandas when reading a csv - Stack Overflow](https://stackoverflow.com/questions/20107570/removing-index-column-in-pandas-when-reading-a-csv)


 

```python
df.to_csv(filename, index=False)
df.read_csv(filename, index=False)  
```
