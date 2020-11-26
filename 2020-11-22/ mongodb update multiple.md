###  mongodb update multiple





 

```
db.books.update(
   { stock: { $lte: 10 } },
   { $set: { reorder: true } },
   { multi: true }
)


db.getCollection('Task').update(
   { status: "DONE" },
   { $set: { status: "ARCHIVED" } },
   { multi: true }
)

```
