### python pandas apply function to dataframe


[python - How can I use the apply() function for a single column? - Stack Overflow](https://stackoverflow.com/questions/34962104/how-can-i-use-the-apply-function-for-a-single-column "python - How can I use the apply() function for a single column? - Stack Overflow")


 

```
  import pandas as pd

  def complex_function(x, y=0):
      if x > 5 and x > y:
          return 1
      else:
          return 2

  df = pd.DataFrame(data={'col1': [1, 4, 6, 2, 7], 'col2': [6, 7, 1, 2, 8]})

  df['col1'] = df['col1'].apply(complex_function)

```
