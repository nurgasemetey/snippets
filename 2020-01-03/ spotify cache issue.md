###  spotify cache issue


[Solved: Re: Linux Cache Location not being respected - The Spotify Community](https://community.spotify.com/t5/Desktop-Linux/Linux-Cache-Location-not-being-respected/m-p/1266695#M4113 "Solved: Re: Linux Cache Location not being respected - The Spotify Community")


 

```
rm -rf $HOME/.cache/spotify
ln -s /media/storage/spotify_cache $HOME/.cache/spotify
```
