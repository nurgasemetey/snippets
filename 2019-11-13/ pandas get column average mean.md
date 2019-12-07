###  pandas get column average/mean


[python - pandas get column average/mean - Stack Overflow](https://stackoverflow.com/questions/31037298/pandas-get-column-average-mean "python - pandas get column average/mean - Stack Overflow")


 

```python
In [479]: df
Out[479]: 
         ID  birthyear    weight
0    619040       1962  0.123123
1    600161       1963  0.981742
2  25602033       1963  1.312312
3    624870       1987  0.942120

In [480]: df["weight"].mean()
Out[480]: 0.83982437500000007
```
