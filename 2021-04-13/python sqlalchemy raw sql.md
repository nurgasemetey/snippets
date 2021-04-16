### python sqlalchemy raw sql


[python - How to execute raw SQL in Flask-SQLAlchemy app - Stack Overflow](https://stackoverflow.com/questions/17972020/how-to-execute-raw-sql-in-flask-sqlalchemy-app "python - How to execute raw SQL in Flask-SQLAlchemy app - Stack Overflow")


 

```
for r in result:
    print(r[0]) # Access by positional index
    print(r['my_column']) # Access by column name as a string
    r_dict = dict(r.items()) # convert to dict keyed by column names


from collections import namedtuple

Record = namedtuple('Record', result.keys())
records = [Record(*r) for r in result.fetchall()]
for r in records:
    print(r.my_column)
    print(r)


result = db.execute('SELECT count(*) as total_count from accidents')
    one_row = result.first()
    #pydantic can be used
    r_dict = dict(one_row.items())
    return r_dict
```
