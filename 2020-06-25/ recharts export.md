###  recharts export


[Downloading charts from client side? · Issue #1027 · recharts/recharts](https://github.com/recharts/recharts/issues/1027 "Downloading charts from client side? · Issue #1027 · recharts/recharts")


 

```js
import domtoimage from 'dom-to-image';
import fileDownload from "js-file-download";

class myComponent extends Component {

handleSaveClick = () => {
 domtoimage.toBlob(document.getElementById('node-to-convert'), {bgColor:"#ffffff"})
    .then(function (blob) {
       fileDownload(blob, 'dom-to-image.png');
    });
}
render() {
   return (
        <div>
          <div id="node-to-convert">
              <!-- your chart content -->
          </div>
         <button onClick={this.handleSaveClick}>save</button>
         </div>
      ) 
}

}
```
