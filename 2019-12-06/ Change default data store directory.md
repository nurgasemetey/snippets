###  Change default data store directory


[How to &quot;change the default Cassandra data store directory&quot; – Interset Knowledge Base](https://interset.zendesk.com/hc/en-us/articles/360001083007-How-to-change-the-default-Cassandra-data-store-directory- "How to &quot;change the default Cassandra data store directory&quot; – Interset Knowledge Base")


 

```shell
Create a new data store directory for Cassandra in a desired location, and it is sized appropriately to accommodate the Cassandra data. Below is an example command:
EXAMPLE: sudo mkdir /data/cassandra
Under the new Cassandra directory, create the follow directories:
data
EXAMPLE: sudo mkdir /data/cassandra/data
commitlog
EXAMPLE: sudo mkdir /data/cassandra/commitlog
saved_caches
EXAMPLE: sudo mkdir /data/cassandra/saved_caches
```
