###  http-proxy usage in nodejs





 

```js
var http = require('http'), httpProxy = require('http-proxy');
var url = require('url');
var modifyResponse = require('node-http-proxy-json');
var _ = require('lodash');

//
// Create a proxy server with custom application logic
//
var proxy = httpProxy.createProxyServer({});

//
// Create your custom server and just call `proxy.web()` to proxy
// a web request to the target passed in the options
// also you can use `proxy.ws()` to proxy a websockets request
//

var option = {
  // target: 'http://127.0.0.1:80',
  target: 'http://geoserver:8080'

  // selfHandleResponse : true
};
proxy.on('proxyRes', function (proxyRes, req, res) {
  modifyResponse(res, proxyRes, function (body) {
    if (body) {
      // modify some information
      body.age = 2;
      delete body.version;
    }
    //parse query params
    var queryData = url.parse(req.url, true).query;
    // if propertyname is empty then don't filter
    if (!queryData.propertyName) {
      return Promise.resolve(body);
    }
    else {
      var fields = ["bbox"].concat(queryData.propertyName.split(","));
      var features = _.map(body.features, function (feature) {
        feature.properties = _.pick(feature.properties, fields);
        return feature;
      });
      body.features = features;
      return Promise.resolve(body);
    }
    // var filteredCollection = _.map(body.features, function (c) {
    //   return _.omit(c, ['name']);
    // });


  });

});

var server = http.createServer(function (req, res) {
  // You can define here your custom logic to handle the request
  // and then proxy the request.

  proxy.web(req, res, option);
});

console.log("listening on port 5050")
server.listen(5050);
```
