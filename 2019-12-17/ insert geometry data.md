###  insert geometry data


[MYSQL-how to insert geometry data - Stack Overflow](https://stackoverflow.com/questions/53466771/mysql-how-to-insert-geometry-data "MYSQL-how to insert geometry data - Stack Overflow")


 

```sql
CREATE TABLE CARTESIAN
(
ROW_ID INT NOT NULL,
G GEOMETRY,
PRIMARY KEY(ROW_ID)
);
INSERT INTO CARTESIAN
VALUES (0,ST_GeomFromText('POINT(1 1)')), 
       (1,ST_GeomFromText('LINESTRING(2 1, 6 6)')), 
       (2,ST_GeomFromText('POLYGON((0 5, 2 5, 2 7, 0 7, 0 5))'));
SELECT * FROM CARTESIAN
```
