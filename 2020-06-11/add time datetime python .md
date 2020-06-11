### add time datetime python 


[Adding Dates and Times in Python | Pressing the Red Button](http://www.pressthered.com/adding_dates_and_times_in_python/ "Adding Dates and Times in Python | Pressing the Red Button")


 

```
from datetime import datetime  
from datetime import timedelta  
  
#Add 1 day  
print datetime.now() + timedelta(days=1)  
  
#Subtract 60 seconds  
print datetime.now() - timedelta(seconds=60)  
  
#Add 2 years  
print datetime.now() + timedelta(days=730)  
```
