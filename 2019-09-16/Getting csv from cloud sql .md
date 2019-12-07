### Getting csv from cloud sql 





 

```shell
gcloud sql export csv gis gs://parabol_ftp_test/test.csv  --database=smart-mobility --query="select start_node from turkey_segments"
```
