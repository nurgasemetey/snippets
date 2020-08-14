### pandas empty column


[python - How to add an empty column to a dataframe? - Stack Overflow](https://stackoverflow.com/questions/16327055/how-to-add-an-empty-column-to-a-dataframe "python - How to add an empty column to a dataframe? - Stack Overflow")




```
if 'Met' not in df:
    df['Met'] = df['freqC'] * df['coverage'] 

if "OSM_START_NODE" not in vehicle_augmented:
     vehicle_augmented["OSM_START_NODE"] = np.nan
if "OSM_FINISH_NODE" not in vehicle_augmented:
     vehicle_augmented["OSM_FINISH_NODE"] = np.nan
```
