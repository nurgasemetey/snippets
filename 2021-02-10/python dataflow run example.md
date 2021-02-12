### python dataflow run example





 

```
python -m apache_beam.examples.wordcount \
  --project project \
  --runner DataflowRunner \
  --temp_location gs://project/location \
  --output gs://project/location \
  --job_name dataflow-intro
```
