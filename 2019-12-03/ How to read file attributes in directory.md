###  How to read file attributes in directory


[python - How to read file attributes in directory? - Stack Overflow](https://stackoverflow.com/questions/10960477/how-to-read-file-attributes-in-directory "python - How to read file attributes in directory? - Stack Overflow")


 

```python
from pathlib import Path

for path in Path('.').iterdir():
    info = path.stat()
    print(info.st_mtime)
```
