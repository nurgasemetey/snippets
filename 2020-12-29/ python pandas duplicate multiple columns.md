###  python pandas duplicate multiple columns


[pandas - Python Find duplicates across multiple columns - Stack Overflow](https://stackoverflow.com/questions/49080143/python-find-duplicates-across-multiple-columns "pandas - Python Find duplicates across multiple columns - Stack Overflow")


 

```
duplicates = data[data.duplicated(subset=['arac_id', 'tarih'], keep=False)]

df = df[df.duplicated(subset=['val1','val2'], keep=False)]


Example dataframe:

col1 col2 col3
A1    B1   C1
A1    B1   C1
A1    B1   C2
A2    B2   C2
Expected output:

col1 col2 col3
A1    B1   C1
A1    B1   C1

```
