###  opencv size matrix height width


[Size of Matrix OpenCV - Stack Overflow](https://stackoverflow.com/questions/14028193/size-of-matrix-opencv "Size of Matrix OpenCV - Stack Overflow")


 

```
cv:Mat mat;
int rows = mat.rows;
int cols = mat.cols;

cv::Size s = mat.size();
rows = s.height;
cols = s.width;
```
