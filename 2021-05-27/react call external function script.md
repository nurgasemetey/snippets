### react call external function script


[reactjs - Call external Javascript function from react components - Stack Overflow](https://stackoverflow.com/questions/35082047/call-external-javascript-function-from-react-components "reactjs - Call external Javascript function from react components - Stack Overflow")


 

```
<script type="text/javascript">
  function test(){
    alert('Function from index.html');
  }
</script>

---
componentWillMount() {
  window.test();
}

---


setCode(window.js_beautify(str));
```
