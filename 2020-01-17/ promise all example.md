###  promise all example


[All you need to know about Promise.all](https://www.freecodecamp.org/news/promise-all-in-javascript-with-example-6c8c5aea3e32/ "All you need to know about Promise.all")


 

```js
        var attachments = files.file.map((fileInfo) => {
            console.log(fileInfo);
            if (!fileInfo.headers["content-type"].startsWith("image/")) {
                errorOccurred = true;
                res.status(400).send({ message: "UPLOAD OF NON-IMAGE ATTACHMENTS IS FORBIDDEN" });
                return;
            }

            // return fileInfo.path;
            return new Promise((resolve, reject) => {
                Storage.saveBase64ToCloudStorage(fileInfo.path, IMAGE_BUCKET_NAME)
                    .then((url) => resolve(url))
                    .catch((err) => reject(err));
            })
        });
        if (errorOccurred) {
            return;
        }
        Promise.all(attachments)
            .then((imageUrls) => {
                // res.status(200).send({imageUrls:imageUrls});
                incomingPostData.imageUrls = imageUrls; 
                FeedbackModel.saveFeedbacks(incomingPostData)
                    .then(saveResult => {
                        res.status(200).json(incomingPostData);
                    })
                    .catch(err => {
                        res.status(400).json(err);
                    });
                return;
            })
            .catch((error) => {
                console.log(`Error in promises ${error}`);
                res.status(400).send({ err: error });
                return;
            });

```
