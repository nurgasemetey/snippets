###  pandas add column if does not exist


[python - Pandas: Add column if does not exists - Stack Overflow](https://stackoverflow.com/questions/25896453/pandas-add-column-if-does-not-exists/25896592 "python - Pandas: Add column if does not exists - Stack Overflow")


 

```
if 'Met' not in df:
    df['Met'] = df['freqC'] * df['coverage'] 

if "OSM_START_NODE" not in vehicle_augmented:
     vehicle_augmented["OSM_START_NODE"] = np.nan
if "OSM_FINISH_NODE" not in vehicle_augmented:
     vehicle_augmented["OSM_FINISH_NODE"] = np.nan
```
