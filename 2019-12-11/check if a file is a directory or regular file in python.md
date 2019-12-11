### check if a file is a directory or regular file in python


[how to check if a file is a directory or regular file in python? - Stack Overflow](https://stackoverflow.com/questions/3204782/how-to-check-if-a-file-is-a-directory-or-regular-file-in-python "how to check if a file is a directory or regular file in python? - Stack Overflow")




```python
os.path.isfile("bob.txt") # Does bob.txt exist?  Is it a file, or a directory?
os.path.isdir("bob")
```
