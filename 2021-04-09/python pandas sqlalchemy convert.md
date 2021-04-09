### python pandas sqlalchemy convert


[python - How can I convert Sqlalchemy table object to Pandas DataFrame? - Stack Overflow](https://stackoverflow.com/questions/25264510/how-can-i-convert-sqlalchemy-table-object-to-pandas-dataframe "python - How can I convert Sqlalchemy table object to Pandas DataFrame? - Stack Overflow")


 

```
import pandas as pd

cols = [c.name for c in SQLA_Table.__table__.columns]
pk = [c.name for c in SQLA_Table.__table__.primary_key]
tuplefied_list = [(getattr(item, col) for col in cols) for item in result_list]

df = pd.DataFrame.from_records(tuplefied_list, index=pk, columns=cols)

```
