###  nodejs export import many variables multiple


[node.js - How do I import many variables at once in javascript in NodeJS? - Stack Overflow](https://stackoverflow.com/questions/34683391/how-do-i-import-many-variables-at-once-in-javascript-in-nodejs/34683462 "node.js - How do I import many variables at once in javascript in NodeJS? - Stack Overflow")



[javascript - Getting Unexpected Token Export - Stack Overflow](https://stackoverflow.com/questions/38296667/getting-unexpected-token-export "javascript - Getting Unexpected Token Export - Stack Overflow")


 You are using ES6 Module syntax.



This means your environment (e.g. node.js) must support ES6 Module syntax.



NodeJS uses CommonJS Module syntax (module.exports) not ES6 module syntax (export keyword).





```
module.exports = {getUser, getSavedTracks, 
  createPlaylist, addTracksToPlaylistBody,
  getPlaylist,getPlaylistTracks
}

const { getPlaylist, getSavedTracks, getPlaylistTracks, getUser,createPlaylist, addTracksToPlaylistBody } = require('./spotify');

```
