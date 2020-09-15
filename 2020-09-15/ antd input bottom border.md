###  antd input bottom border


[html - Input text field with only bottom border - Stack Overflow](https://stackoverflow.com/questions/37465458/input-text-field-with-only-bottom-border/37465540 "html - Input text field with only bottom border - Stack Overflow")


 

```
input {
    border: 0;
    outline: 0;
    border-bottom: 2px solid blue;
}

---

<Input 
            size="large" 
            placeholder="Your input" 
            prefix={<UserOutlined />} 
            bordered={false}  
            style={{
                borderBottom:"2px solid black"
                }}
            />
```
