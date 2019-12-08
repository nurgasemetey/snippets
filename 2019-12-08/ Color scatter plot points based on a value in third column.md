###  Color scatter plot points based on a value in third column


[python - Color scatter plot points based on a value in third column? - Stack Overflow](https://stackoverflow.com/questions/42660810/color-scatter-plot-points-based-on-a-value-in-third-column "python - Color scatter plot points based on a value in third column? - Stack Overflow")


 

```python 
plt.scatter(waterUsage['duration'], waterUsage['water_amount'],\
            c=waterUsage['third_column'], cmap=plt.cm.autumn)
```
