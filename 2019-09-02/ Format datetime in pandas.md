###  Format datetime in pandas


[python - How to define format when use pandas to_datetime? - Stack Overflow](https://stackoverflow.com/questions/36848514/how-to-define-format-when-use-pandas-to-datetime)


 Format is explained here : [Python string to datetime - strptime() - JournalDev](https://www.journaldev.com/23365/python-string-to-datetime-strptime)

```python
df['TIME'] = pd.to_datetime(df['TIME'], format="%m/%d/%Y %I:%M:%S %p")

```

