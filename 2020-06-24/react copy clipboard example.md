### react copy clipboard example


[nkbt/react-copy-to-clipboard: Copy-to-clipboard React component](https://github.com/nkbt/react-copy-to-clipboard "nkbt/react-copy-to-clipboard: Copy-to-clipboard React component")




```js
 <CopyToClipboard text={this.state.value}
          onCopy={() => this.setState({copied: true})}>
          <span>Copy to clipboard with span</span>
        </CopyToClipboard>



                    <CopyToClipboard text={url} 
                    onCopy={() => message.success("You copied")}
                    >
                        <Button size="large" icon={<CopyOutlined style={{ fontSize: '20px' }} />}>Copy</Button>
                    </CopyToClipboard>
```
