### error handling in express and typescript


[TypeScript Express tutorial #3. Express error handling &amp; validating data](https://wanago.io/2018/12/17/typescript-express-error-handling-validation/ "TypeScript Express tutorial #3. Express error handling &amp; validating data")




```typescript
class HttpException extends Error {
  status: number;
  message: string;
  constructor(status: number, message: string) {
    super(message);
    this.status = status;
    this.message = message;
  }
}
 
export default HttpException;


import { NextFunction, Request, Response } from 'express';
import HttpException from '../exceptions/HttpException';
 
function errorMiddleware(error: HttpException, request: Request, response: Response, next: NextFunction) {
  const status = error.status || 500;
  const message = error.message || 'Something went wrong';
  response
    .status(status)
    .send({
      status,
      message,
    })
}
 
export default errorMiddleware;



new HttpException(400, message))

```
