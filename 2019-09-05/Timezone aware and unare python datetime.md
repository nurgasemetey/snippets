### Timezone aware and unare python datetime


[How to make an unaware datetime timezone aware in python - Stack Overflow](https://stackoverflow.com/questions/7065164/how-to-make-an-unaware-datetime-timezone-aware-in-python)


 

```python
#I had use from dt_aware to dt_unaware

dt_unaware = dt_aware.replace(tzinfo=None)

#and dt_unware to dt_aware

from pytz import timezone
localtz = timezone('Europe/Lisbon')
dt_aware = localtz.localize(dt_unware)

```
