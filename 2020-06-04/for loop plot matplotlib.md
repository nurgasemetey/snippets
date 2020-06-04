### for loop plot matplotlib


[python - savefig loop adds previous plots to figure - Stack Overflow](https://stackoverflow.com/questions/37734512/savefig-loop-adds-previous-plots-to-figure "python - savefig loop adds previous plots to figure - Stack Overflow")




```python
ax = df.plot(kind='bar',x="segment_id",y="gps_count", title =f'GPS count augmented {interval}-{direction}', figsize=(15, 10), legend=True, fontsize=12)
    ax.set_xlabel("segment_id", fontsize=12)
    ax.set_ylabel("gps_count", fontsize=12)
    n=49
    ticks = ax.xaxis.get_ticklocs()
    ticklabels = [l.get_text() for l in ax.xaxis.get_ticklabels()]
    ax.xaxis.set_ticks(ticks[::n])
    ax.xaxis.set_ticklabels(ticklabels[::n])
    plt.savefig(f'gps-count-augmented-{interval}-{direction}.svg', format="svg")
    plt.close()
```
