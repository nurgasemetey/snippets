### mongo nodejs simple example 





 

```
const MongoClient = require('mongodb').MongoClient;

const url = 'mongodb://user:password@ip:port/db';
const dbName = 'db';

async function run() {
  try {
    const client = await MongoClient.connect(url);
    // console.log(client);
    const db = client.db(dbName);
    const junctionArchiveInfoCollection = db.collection('junctionArchiveInfo');
    const phaseDataArchiveCollection = db.collection('phaseDataArchiveCollection');
    const junctionArchiveInfoArr = await junctionArchiveInfoCollection.find({}).toArray();
    for (const junctionArchiveInfo of junctionArchiveInfoArr) {
      console.log(junctionArchiveInfo);
      const phaseDataArchiveData = await phaseDataArchiveCollection.aggregate([{
        $match:{
          junctionId:junctionArchiveInfo["versionId"]
          // junctionId:"59de3886e4b01ac57a8bea98"
        }
      }]).toArray();
      console.log(phaseDataArchiveData)
      break;
    }
    client.close();
  } catch(err) {
    console.log(err);
  }
}

run().then().catch();
```
