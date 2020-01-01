###  change region in gcloud


[How to change Region / Zone in Google Cloud? - Stack Overflow](https://stackoverflow.com/questions/45125143/how-to-change-region-zone-in-google-cloud "How to change Region / Zone in Google Cloud? - Stack Overflow")


 

```shell

Use commands below at cloud shell.

To check your preferred region:

$ gcloud compute regions list
To change compute regions, I select us-east4 region:

$ gcloud config set compute/region us-east4
Updated property [compute/region].

$ gcloud config list compute/region 
[compute]

region = us-east4
In a similar way, you can change compute/zone.
```
