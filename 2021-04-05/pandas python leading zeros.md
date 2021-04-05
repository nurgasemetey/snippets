### pandas python leading zeros


[python - Add Leading Zeros to Strings in Pandas Dataframe - Stack Overflow](https://stackoverflow.com/questions/23836277/add-leading-zeros-to-strings-in-pandas-dataframe "python - Add Leading Zeros to Strings in Pandas Dataframe - Stack Overflow")


 

```
df['ID'] = df['ID'].apply(lambda x: '{0:0>15}'.format(x))

```
