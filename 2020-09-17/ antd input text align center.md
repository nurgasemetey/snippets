###  antd input text align center


[javascript - How to centralize text in textinput - Stack Overflow](https://stackoverflow.com/questions/30012089/how-to-centralize-text-in-textinput "javascript - How to centralize text in textinput - Stack Overflow")


 

```
<Input
                                size="large"
                                placeholder="Your input"
                                value={input}
                                // prefix={<UserOutlined />}
                                bordered={false}
                                onChange={(e) => {
                                    this.setState({input:e.target.value});
                                }}
                                onPressEnter={this.addWeekDecision}
                                style={{
                                    borderBottom: "2px solid black",
                                    fontSize: 40,
                                    textAlign:"center"
                                }}
                            />
```
