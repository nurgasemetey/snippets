###  bar plot pandas matplotlib tick


[python - Pandas: bar plot xtick frequency - Stack Overflow](https://stackoverflow.com/questions/19143857/pandas-bar-plot-xtick-frequency?answertab=oldest#tab-top "python - Pandas: bar plot xtick frequency - Stack Overflow")


 

```python
    df = pd.DataFrame(segment_occurence_list, columns=["segment_id", "gps_count"]);
    df = df.sort_values(by=['segment_id'])
    ax = df.plot(kind='bar',x="segment_id",y="gps_count", title =f'GPS count augmented {interval}-{direction}', figsize=(15, 10), legend=True, fontsize=12)
    ax.set_xlabel("segment_id", fontsize=12)
    ax.set_ylabel("gps_count", fontsize=12)
    n=49
    ticks = ax.xaxis.get_ticklocs()
    ticklabels = [l.get_text() for l in ax.xaxis.get_ticklabels()]
    ax.xaxis.set_ticks(ticks[::n])
    ax.xaxis.set_ticklabels(ticklabels[::n])
```
