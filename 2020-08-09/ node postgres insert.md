###  node postgres insert


[Integrating PostgreSQL with Node.js and node-postgres](https://stackabuse.com/using-postgresql-with-nodejs-and-node-postgres/ "Integrating PostgreSQL with Node.js and node-postgres")



[Queries | node-postgres](https://node-postgres.com/features/queries "Queries | node-postgres")


 

```
      const query = {
        text: 'INSERT INTO user_playlist(user_id, playlist_id, sync_playlist_id) VALUES($1, $2, $3) ON CONFLICT (user_id,playlist_id) DO UPDATE SET sync_playlist_id = excluded.sync_playlist_id RETURNING *',
        values: [userData.id, req.body.playlistId, commonPlaylist.id],
      }
      const { rows }= await client.query(query);
```
