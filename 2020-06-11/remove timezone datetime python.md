### remove timezone datetime python


[python - How can I remove a pytz timezone from a datetime object? - Stack Overflow](https://stackoverflow.com/questions/10944047/how-can-i-remove-a-pytz-timezone-from-a-datetime-object "python - How can I remove a pytz timezone from a datetime object? - Stack Overflow")


 

```
                date_start = datetime.fromisoformat(date_start_str)
                date_start = date_start.replace(tzinfo=None)
                print(date_start)
                print(date_start.tzinfo)
```
