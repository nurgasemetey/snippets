### Exporting data from Cloud SQL


[Exporting data from Cloud SQL | Cloud SQL for MySQL | Google Cloud](https://cloud.google.com/sql/docs/mysql/import-export/exporting)




```shell
gcloud sql export sql [INSTANCE_NAME] gs://[BUCKET_NAME]/sqldumpfile.gz \
                            --database=[DATABASE_NAME]
```
