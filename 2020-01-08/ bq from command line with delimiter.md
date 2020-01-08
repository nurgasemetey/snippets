###  bigquery from command line with delimiter


[Loading CSV data from Cloud Storage | BigQuery | Google Cloud](https://cloud.google.com/bigquery/docs/loading-data-cloud-storage-csv#loading_csv_data_into_a_new_table "Loading CSV data from Cloud Storage  |  BigQuery  |  Google Cloud")




```shell
bq load --field_delimiter=';' --source_format=CSV public-transportation-tto:fcd.segment_data_tmp "gs://parabol_third-party-segment-travel-time/*.csv" schema_tmp.json


bq load --field_delimiter=';' --source_format=CSV public-transportation-tto:fcd.segment_data_tmp /home/nurgasemetey/Downloads/2019-04-30T20_58_00-turkey-east.csv schema_tmp.json
```

