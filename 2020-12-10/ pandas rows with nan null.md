###  pandas rows with nan null


[python - How to select rows with NaN in particular column? - Stack Overflow](https://stackoverflow.com/questions/43831539/how-to-select-rows-with-nan-in-particular-column "python - How to select rows with NaN in particular column? - Stack Overflow")


 

```
df[df['Col2'].isnull()]
all_stops[all_stops['KOORDINAT_Y'].isnull()]

```
