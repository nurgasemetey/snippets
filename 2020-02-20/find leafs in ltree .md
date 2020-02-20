### find leafs in ltree 


[performance - How do I find the leafs using PostgreSQL's ltree? - Database Administrators Stack Exchange](https://dba.stackexchange.com/questions/175016/how-do-i-find-the-leafs-using-postgresqls-ltree "performance - How do I find the leafs using PostgreSQL's ltree? - Database Administrators Stack Exchange")




```sql
CREATE TABLE foo(ltree)
AS
  VALUES
    ( 'Top.Science.Astronomy'::ltree ),
    ( 'Top.Science.Astronomy.Astrophysics' ),
    ( 'Top.Science.Astronomy.Cosmology' ),
    ( 'Top.Collections.Pictures.Astronomy' ),
    ( 'Top.Collections.Pictures.Astronomy.Stars' ),
    ( 'Top.Collections.Pictures.Astronomy.Galaxies' ),
    ( 'Top.Collections.Pictures.Astronomy.Astronauts' );

CREATE INDEX ON foo USING gist(ltree);

SELECT *
FROM foo AS f1
WHERE NOT EXISTS (
  SELECT 1
  FROM foo AS f2
  WHERE f1.ltree <> f2.ltree
    AND f1.ltree @> f2.ltree
);
```
