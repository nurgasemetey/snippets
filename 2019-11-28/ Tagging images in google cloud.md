###  Tagging images in google cloud


[Managing images | Container Registry | Google Cloud](https://cloud.google.com/container-registry/docs/managing#tagging_images "Managing images  |  Container Registry  |  Google Cloud")


 

```shell
gcloud container images list-tags eu.gcr.io/metistraffic-218311/gateway


gcloud container images add-tag eu.gcr.io/metistraffic-218311/gateway@sha256:ac7690abc4e868c83471efae51422e18da31388155cb6d65a8c362fbdde50e08 eu.gcr.io/metistraffic-218311/gateway:konya
```
