### pandas combine columns in new column



[python - Combine two columns of text in pandas dataframe - Stack Overflow](https://stackoverflow.com/questions/19377969/combine-two-columns-of-text-in-pandas-dataframe "python - Combine two columns of text in pandas dataframe - Stack Overflow")




```
trip_data["linkId.timeBin"] = trip_data['linkId'].astype(str) + "." + trip_data['timeBin']


```
