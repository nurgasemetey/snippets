### Getting csv from cloud sql 





 

```shell
gcloud sql export csv gis gs://bucket/test.csv  --database=smart-mobility --query="select start_node from turkey_segments"
```
