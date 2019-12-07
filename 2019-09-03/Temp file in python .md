### Temp file in python 


[Python - writing and reading from a temporary file - Stack Overflow](https://stackoverflow.com/questions/39983886/python-writing-and-reading-from-a-temporary-file)


 

```python
import tempfile

tmp = tempfile.NamedTemporaryFile()

# Open the file for writing.
with open(tmp.name, 'w') as f:
    f.write(stuff) # where `stuff` is, y'know... stuff to write (a string)

...

# Open the file for reading.
with open(tmp.name) as f:
    for line in f:
        ... # more things here
```
