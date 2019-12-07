###  Importing custom module into jupyter notebook


[python - Importing custom module into jupyter notebook - Stack Overflow](https://stackoverflow.com/questions/53049195/importing-custom-module-into-jupyter-notebook/59046530#59046530 "python - Importing custom module into jupyter notebook - Stack Overflow")


 

```shell
import sys
sys.path.append('../src/')

from my_module import helpers


---
project/
    │
    ├── src/
    │    └── my_module/
    │        ├── __init__.py       
    │        └── helpers.py
    ├── notebooks/
    │   └── a_notebook.ipynb
    ...
```
