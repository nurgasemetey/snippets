###  node-postgres nodejs pool connect await


[node-postgres connection and query with async/await](https://gist.github.com/zerbfra/70b155fa00b4e0d6fd1d4e090a039ad4 "node-postgres connection and query with async/await")



[Integrating PostgreSQL with Node.js and node-postgres](https://stackabuse.com/using-postgresql-with-nodejs-and-node-postgres/ "Integrating PostgreSQL with Node.js and node-postgres")


 

```
const Pool = require('pg').Pool
const pool = new Pool({
  user: 'postgres',
  host: 'localhost',
  database: 'spotify_playlist_manager',
  password: 'admin',
  port: 5432,
})


let client = null;
const connect = async () => {
  try{
    client = await pool.connect();
    // console.log(client);
  } catch(err) {
    console.log("Error");
  }
}
```
