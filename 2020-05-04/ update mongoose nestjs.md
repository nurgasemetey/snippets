###  update mongoose nestjs


[nest-blog-app/blog.service.ts at a445a54c6d498d73f2acbcc8c22c16a84906b3b4 · mahmutkaya/nest-blog-app](https://github.com/mahmutkaya/nest-blog-app/blob/a445a54c6d498d73f2acbcc8c22c16a84906b3b4/blog-backend/src/blog/blog.module.ts "nest-blog-app/blog.service.ts at a445a54c6d498d73f2acbcc8c22c16a84906b3b4 · mahmutkaya/nest-blog-app")


 

```js
async editPost(postID, createPostDTO: CreatePostDTO): Promise<Post> {
        const editedPost = await this.postModel.findByIdAndUpdate(postID, createPostDTO, { new: true });
        return editedPost;
    }
```
