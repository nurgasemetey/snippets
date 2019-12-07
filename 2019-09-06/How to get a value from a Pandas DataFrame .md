### How to get a value from a Pandas DataFrame 


[python - How to get a value from a Pandas DataFrame and not the index and object type - Stack Overflow](https://stackoverflow.com/questions/30787901/how-to-get-a-value-from-a-pandas-dataframe-and-not-the-index-and-object-type)


 

```python
Letter    Number
A          1
B          2
C          3
D          4



df[df.Letters=='C'].Letters.item()

```
