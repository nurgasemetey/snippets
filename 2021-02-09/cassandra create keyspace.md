### cassandra create keyspace







```
CREATE KEYSPACE iot WITH REPLICATION = { 'class' : 'org.apache.cassandra.locator.SimpleStrategy', 'replication_factor': '1' } AND DURABLE_WRITES = true;
use keyspaces;
```
