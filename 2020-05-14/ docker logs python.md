###  docker logs python


[Python app does not print anything when running detached in docker - Stack Overflow](https://stackoverflow.com/questions/29663459/python-app-does-not-print-anything-when-running-detached-in-docker "Python app does not print anything when running detached in docker - Stack Overflow")


 

```
in Dockerfile
Using unbuffered output with

CMD ["python","-u","main.py"]
instead of

CMD ["python","main.py"]
```
