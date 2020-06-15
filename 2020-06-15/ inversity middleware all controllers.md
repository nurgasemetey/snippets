###  inversity middleware all controllers


[Inversify-Express-Utils Middleware for all controllers · Issue #852 · inversify/InversifyJS](https://github.com/inversify/InversifyJS/issues/852 "Inversify-Express-Utils Middleware for all controllers · Issue #852 · inversify/InversifyJS")


 

```
function myMiddleWare(request: express.Request, response: express.Response, next: express.NextFunction) {
    console.log(`HTTP ${request.method} ${request.url}`);
    next();
}

let server = new InversifyExpressServer(container);

server.setConfig((app) => {
  app.use(myMiddleWare);
  app.use(bodyParser.json());
});

let serverInstance = server.build();
serverInstance.listen(3000);
```
