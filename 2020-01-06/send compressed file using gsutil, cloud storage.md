### send compressed file using gsutil, cloud storage


[How do I unzip a .zip file in google cloud storage? - Stack Overflow](https://stackoverflow.com/questions/49541026/how-do-i-unzip-a-zip-file-in-google-cloud-storage "How do I unzip a .zip file in google cloud storage? - Stack Overflow")




```shell
gsutil cp -Z largefile.txt gs://bucket/largefile.txt

```
