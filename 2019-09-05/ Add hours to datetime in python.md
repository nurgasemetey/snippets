###  Add hours to datetime in python


[How to add hours to current time in python - Stack Overflow](https://stackoverflow.com/questions/13685201/how-to-add-hours-to-current-time-in-python)


 

```python
from datetime import datetime, timedelta

nine_hours_from_now = datetime.now() + timedelta(hours=9)
```
