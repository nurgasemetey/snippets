### Correct way to try/except using Python requests module 


[Correct way to try/except using Python requests module? - Stack Overflow](https://stackoverflow.com/questions/16511337/correct-way-to-try-except-using-python-requests-module "Correct way to try/except using Python requests module? - Stack Overflow")


 

```python
url='http://www.google.com/blahblah'

try:
    r = requests.get(url,timeout=3)
    r.raise_for_status()
except requests.exceptions.HTTPError as errh:
    print ("Http Error:",errh)
except requests.exceptions.ConnectionError as errc:
    print ("Error Connecting:",errc)
except requests.exceptions.Timeout as errt:
    print ("Timeout Error:",errt)
except requests.exceptions.RequestException as err:
    print ("OOps: Something Else",err)
```
