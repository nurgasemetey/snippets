###  Update many example typeorm


[advanced-testing-example/server.ts at 0284eb282347445b871ac64174b322497480bd56 · liwoo/advanced-testing-example](https://github.com/liwoo/advanced-testing-example/blob/0284eb282347445b871ac64174b322497480bd56/src/server.ts)


 

```javascript
const repository = getMongoRepository(Developer, dbMode);
      await repository.deleteMany({});

      //Write to DB Operations
      const developers: Developer[] = await repository.save(req.body);
      const bodyChunks = chunk(developers, 100);

      //Migrate Operation
      for (const bodyChunk of bodyChunks) {
        const apiResp = await fakeApi.post(bodyChunk);
        const searchIDs = bodyChunk.map(bc => bc._id);
        // const devsfromDB = await Developer.findByIds(searchIDs);
        if (apiResp) {
          await repository.updateMany(
            { _id: { $in: searchIDs } },
            { $set: { migratedAt: Date.now().toString() } }
          );
```
