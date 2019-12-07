###  Export google sql as csv





 

```shell
gcloud sql export csv gis gs://parabol_ftp_test/test.csv  --database=smart-mobility --query="select start_node, finish_node, speed from turkey_segments"
```
