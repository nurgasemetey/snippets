###  github action docker build


parabol internal nginx


 

```
# This is a basic workflow to help you get started with Actions

name: CI

# Controls when the action will run. Triggers the workflow on push or pull request
# events but only for the master branch
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]
jobs:
  build-and-push-to-gcr:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2 
    - name: Build and push Docker images
      uses: docker/build-push-action@v1
      with:
          username: _json_key
          password: ${{ secrets.GCLOUD_SERVICE_KEY }}
          registry: eu.gcr.io
          repository: metistraffic-218311/paraboly-internal-nginx
          tags: latest
```
