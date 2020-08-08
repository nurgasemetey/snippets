###  postgresql composite primary key


[sql - Postgres: How to do Composite keys? - Stack Overflow](https://stackoverflow.com/questions/1285967/postgres-how-to-do-composite-keys "sql - Postgres: How to do Composite keys? - Stack Overflow")


 

```
CREATE TABLE tags (
    question_id INTEGER NOT NULL,
    tag_id SERIAL NOT NULL,
    tag1 VARCHAR(20),
    tag2 VARCHAR(20),
    tag3 VARCHAR(20),
    PRIMARY KEY(question_id, tag_id),
);
```
