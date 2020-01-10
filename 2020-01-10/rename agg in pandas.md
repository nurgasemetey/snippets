### rename agg in pandas


[python - Naming returned columns in Pandas aggregate function? - Stack Overflow](https://stackoverflow.com/questions/19078325/naming-returned-columns-in-pandas-aggregate-function/43897124 "python - Naming returned columns in Pandas aggregate function? - Stack Overflow")


 

```python
            test_gr = test_sorted.groupby(pd.Grouper(freq='1H')).agg(
                speed_ma_max=("speed_ma","max"),
                speed_ma_min=("speed_ma","min"),
                length_mm=("length_mm","first"),
                link_id=("link_id","first"),
                order=("order","first"),
                segment_id=("segment_id","first"),
                wkt=("wkt","first"),)
```
