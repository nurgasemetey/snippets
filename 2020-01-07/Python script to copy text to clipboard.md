### Python script to copy text to clipboard


[Python script to copy text to clipboard - Stack Overflow](https://stackoverflow.com/questions/11063458/python-script-to-copy-text-to-clipboard "Python script to copy text to clipboard - Stack Overflow")




```python
import subprocess

def copy2clip(txt):
    cmd='echo '+txt.strip()+'|clip'
    return subprocess.check_call(cmd, shell=True)
```
