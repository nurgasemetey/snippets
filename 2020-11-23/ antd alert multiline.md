###  antd alert multiline


[Multi-line antd alert description - Stack Overflow](https://stackoverflow.com/questions/44362606/multi-line-antd-alert-description "Multi-line antd alert description - Stack Overflow")


 

```
descriptionElement = (
  <code>
    Line 1
    <br />
    Line 2
  </code>
)
<Alert message='test' type='info' description={descriptionElement} />

```
