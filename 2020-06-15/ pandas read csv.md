###  pandas read csv


[Python Pandas read_csv: Load Data from CSV Files | Shane Lynn](https://www.shanelynn.ie/python-pandas-read_csv-load-data-from-csv-files/ "Python Pandas read_csv: Load Data from CSV Files | Shane Lynn")


 

```python
data = pd.read_csv(
    "data/files/complex_data_example.tsv",      # relative python path to subdirectory
    sep='\t'           # Tab-separated value file.
    quotechar="'",        # single quote allowed as quote character
    dtype={"salary": int},             # Parse the salary column as an integer 
    usecols=['name', 'birth_date', 'salary'].   # Only load the three columns specified.
    parse_dates=['birth_date'],     # Intepret the birth_date column as a date
    skiprows=10,         # Skip the first 10 rows of the file
    na_values=['.', '??']       # Take any '.' or '??' values as NA
)
```
