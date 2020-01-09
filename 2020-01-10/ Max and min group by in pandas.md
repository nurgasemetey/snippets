###  Max and min group by in pandas


[python - How I can find out max and min value of each day from hourly data sets - Stack Overflow](https://stackoverflow.com/questions/40500957/how-i-can-find-out-max-and-min-value-of-each-day-from-hourly-data-sets "python - How I can find out max and min value of each day from hourly data sets - Stack Overflow")


 

```python
test_gr = test_sorted.groupby(pd.Grouper(freq='1H')).agg({
                "speed_ma":['min','max'], 
                "length_mm": "first",
                "link_id": "first",
                "order": "first",
                "segment_id": "first"
                })
```
