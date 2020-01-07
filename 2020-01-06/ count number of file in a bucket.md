###  count number of file in a bucket


[google cloud storage - How to count number of file in a bucket-folder with gsutil - Stack Overflow](https://stackoverflow.com/questions/18986379/how-to-count-number-of-file-in-a-bucket-folder-with-gsutil "google cloud storage - How to count number of file in a bucket-folder with gsutil - Stack Overflow")


 

```shell
gsutil du gs://pub | wc -l
```
