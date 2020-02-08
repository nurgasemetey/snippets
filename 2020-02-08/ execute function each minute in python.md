###  execute function each minute in python


[timer - What is the best way to repeatedly execute a function every x seconds in Python? - Stack Overflow](https://stackoverflow.com/questions/474528/what-is-the-best-way-to-repeatedly-execute-a-function-every-x-seconds-in-python "timer - What is the best way to repeatedly execute a function every x seconds in Python? - Stack Overflow")


 

```python
import sched, time
s = sched.scheduler(time.time, time.sleep)
def do_something(sc): 
    print "Doing stuff..."
    # do your stuff
    s.enter(60, 1, do_something, (sc,))

s.enter(60, 1, do_something, (s,))
s.run()
```
