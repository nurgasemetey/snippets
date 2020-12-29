### pandas python remove duplicates multiple columns


[python - Remove duplicates from dataframe, based on two columns A,B, keeping row with max value in another column C - Stack Overflow](https://stackoverflow.com/questions/32093829/remove-duplicates-from-dataframe-based-on-two-columns-a-b-keeping-row-with-max "python - Remove duplicates from dataframe, based on two columns A,B, keeping row with max value in another column C - Stack Overflow")




```
df.drop_duplicates(['A','B'],keep= 'last')
non_duplicated = data.drop_duplicates(['arac_id', 'tarih'],keep= 'first')

```
