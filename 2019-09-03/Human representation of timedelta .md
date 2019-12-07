### Human representation of timedelta 


[python - Format timedelta to string - Stack Overflow](https://stackoverflow.com/questions/538666/format-timedelta-to-string)


 

```python
import humanfriendly
from datetime import timedelta
delta = timedelta(seconds = 321)
humanfriendly.format_timespan(delta)

'5 minutes and 21 seconds'
```
