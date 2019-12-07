### Updating in iterrows


[python - Updating value in iterrow for pandas - Stack Overflow](https://stackoverflow.com/questions/25478528/updating-value-in-iterrow-for-pandas)




```python
for index, row in rche_df.iterrows():
    if isinstance(row.wgs1984_latitude, float):
        row = row.copy()
        target = row.address_chi        
        dict_temp = geocoding(target)
        rche_df.loc[index, 'wgs1984_latitude'] = dict_temp['lat']
        rche_df.loc[index, 'wgs1984_longitude'] = dict_temp['long']
```
