###  evernote smoothing


[\[windows\] Running Evernote in Wine on Linux - Windows Archive - Evernote User Forum](https://discussion.evernote.com/topic/48073-running-evernote-in-wine-on-linux/)


 

```shell
If you stick with wine, there are a few tricks to get EN looking its best (based on ubuntu, but should be generic):

 

1. Install some fonts: 

 

winetricks tahoma

winetricks corefonts

 

2. Configure wine font smoothing

 

wget http://files.polosatus.ru/winefontssmoothing_en.sh
bash winefontssmoothing_en.sh
```
