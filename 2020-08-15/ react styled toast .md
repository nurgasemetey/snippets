###  react styled toast 


[How to style | React-Toastify](https://fkhadra.github.io/react-toastify/how-to-style/#how-to-style-with-styled-components "How to style | React-Toastify")


 

```
const StyledToastContainer = styled(ToastContainer).attrs({
  className: 'toast-container',
  toastClassName: 'toast',
  bodyClassName: 'body',
  progressClassName: 'progress',
})`

   /* .toast is passed to toastClassName */
  .toast {
    background-color: ${colors.grey};
  }

`;
```
