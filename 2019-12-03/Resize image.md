### Resize image


[lovell/sharp: High performance Node.js image processing, the fastest module to resize JPEG, PNG, WebP and TIFF images. Uses the libvips library.](https://github.com/lovell/sharp "lovell/sharp: High performance Node.js image processing, the fastest module to resize JPEG, PNG, WebP and TIFF images. Uses the libvips library.")




```typescript
let thumbnailResizeResult = await sharp(attachment.tmpPath).resize(150, 150).png({}).toFile(thumbnailPath);

```
