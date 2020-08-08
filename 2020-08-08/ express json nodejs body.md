###  express json nodejs body


[Get HTTP POST Body in Express.js](https://stackabuse.com/get-http-post-body-in-express-js/ "Get HTTP POST Body in Express.js")


 

```
npm install body-parser


const bodyParser = require('body-parser');



const app = express();
app.use(bodyParser.urlencoded({ extended: true }));
app.use(bodyParser.json());
app.use(bodyParser.raw());

```
