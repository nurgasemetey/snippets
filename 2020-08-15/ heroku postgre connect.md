###  heroku postgre connect


[Heroku Postgres | Heroku Dev Center](https://devcenter.heroku.com/articles/heroku-postgresql#provisioning-heroku-postgres "Heroku Postgres | Heroku Dev Center")


 

```
if(process.env.DATABASE_URL) {
  pool = new Pool({
    connectionString: process.env.DATABASE_URL,
    ssl: {
      rejectUnauthorized: false
    }
  })
}
```
