### Rename gsutil


[Mass rename objects on Google Cloud Storage - Stack Overflow](https://stackoverflow.com/questions/27166441/mass-rename-objects-on-google-cloud-storage "Mass rename objects on Google Cloud Storage - Stack Overflow")


 

```shell
gsutil ls gs://bucket_name/*.JPG > src-rename-list.txt
gsutil ls gs://bucket_name/*.JPG | sed 's/\.JPG/\.jpg/g' > dest-rename-list.txt
paste -d ' ' src-rename-list.txt dest-rename-list.txt | sed -e 's/^/gsutil\ mv\ /' | while read line; do bash -c "$line"; done
rm src-rename-list.txt; rm dest-rename-list.txt
```
