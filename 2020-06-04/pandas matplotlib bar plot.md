### pandas matplotlib bar plot


[Pandas Dataframe: Plot Examples with Matplotlib and Pyplot](http://queirozf.com/entries/pandas-dataframe-plot-examples-with-matplotlib-pyplot "Pandas Dataframe: Plot Examples with Matplotlib and Pyplot")




```python
    df = pd.DataFrame(segment_occurence_list, columns=["segment_id", "gps_count"]);
    df = df.sort_values(by=['segment_id'])
    ax = df.plot(kind='bar',x="segment_id",y="gps_count", title =f'GPS count augmented {interval}-{direction}', figsize=(15, 10), legend=True, fontsize=12)

```
