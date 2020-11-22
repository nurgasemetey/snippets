###  webm to gif linux


[14.04 - How to do I convert an webm (video) to a (animated) gif on the command line? - Ask Ubuntu](https://askubuntu.com/questions/506670/how-to-do-i-convert-an-webm-video-to-a-animated-gif-on-the-command-line "14.04 - How to do I convert an webm (video) to a (animated) gif on the command line? - Ask Ubuntu")


 

```
ffmpeg -i input.webm -pix_fmt rgb24 output.gif
gifsicle -O2 input.gif -o output.gif
```
