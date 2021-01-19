### kubernetes update image


[How do I force Kubernetes to re-pull an image? - Stack Overflow](https://stackoverflow.com/questions/33112789/how-do-i-force-kubernetes-to-re-pull-an-image "How do I force Kubernetes to re-pull an image? - Stack Overflow")


 

```
My hack during development is to change my Deployment manifest to add the latest tag and always pull like so

image: etoews/my-image:latest
imagePullPolicy: Always

kubectl delete pod my-app-3498980157-2zxhd

```
