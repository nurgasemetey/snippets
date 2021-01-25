### nodejs javascript datastore pagination


[Query - Documentation](https://googleapis.dev/nodejs/datastore/latest/Query.html#start "Query - Documentation")



[Datastore Queries | Cloud Datastore Documentation | Google Cloud](https://cloud.google.com/datastore/docs/concepts/queries#datastore-datastore-cursor-paging-nodejs "Datastore Queries  |  Cloud Datastore Documentation  |  Google Cloud")


 

```
let query = ds.createQuery([kind]);
        if (pageLimit) query.limit(pageLimit);
        if (pageCursor) query.start(pageCursor);
```
