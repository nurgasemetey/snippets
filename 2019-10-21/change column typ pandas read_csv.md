###  change column typ pandas read_csv


[How to Change Data Type for One or More Columns in Pandas Dataframe? — Python and R Tips](https://cmdlinetips.com/2018/09/how-to-change-data-type-for-one-or-more-columns-in-pandas-dataframe/)


 

```python
df = pd.read_csv("weather.tsv", sep="\t",  
                 dtype={'Day': str,'Wind':int64})
```
