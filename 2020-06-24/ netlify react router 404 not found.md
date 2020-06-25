###  netlify react router 404 not found


[reactjs - Catch all redirect for create-react-app in netlify - Stack Overflow](https://stackoverflow.com/questions/55990467/catch-all-redirect-for-create-react-app-in-netlify "reactjs - Catch all redirect for create-react-app in netlify - Stack Overflow")


 Put the _redirects in the /public directory. CRA will copy all files in /public to the build directory when running the build command.



/public/_redirects





```
/* /index.html  200
```
