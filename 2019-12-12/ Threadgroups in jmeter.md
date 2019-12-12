###  Threadgroups in jmeter


[Guide to JMeter Thread Groups](https://www.redline13.com/blog/2018/05/guide-jmeter-thread-groups/ "Guide to JMeter Thread Groups")


 

```
Number Of Threads: It represents the total number of virtual users performing the test script execution.
Ramp-Up Period (in seconds): It tells JMeter how long to take to reach the full number of threads. For example, if you have 100 users with a ramp-up period of 50 seconds, JMeter will take 50 seconds to get all 100 threads running, adding 2 threads per second.
Loop Count: It is the number of executions for the script. For example, if the loop count is 2 and number of threads is 100 then the script will run 200 times. If the loop count is set “forever” then new threads will keep starting until the tests are stopped.
Delay Thread Creation Until Needed: If this option is checked, the ramp-up delay and startup delay are performed before the thread data is created. If not checked, all the data required for the threads is created before starting the execution of a test.
Scheduler: This schedules the tests. You can set custom duration and startup delay to create the threads in this section.
```
