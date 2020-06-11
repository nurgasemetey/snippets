### check tz datetime python


[python - How to check if a datetime object is localized with pytz? - Stack Overflow](https://stackoverflow.com/questions/5802108/how-to-check-if-a-datetime-object-is-localized-with-pytz "python - How to check if a datetime object is localized with pytz? - Stack Overflow")


```python
                date_start = datetime.fromisoformat(date_start_str)
                print(date_start)
                print(date_start.tzinfo)
```
