###  How to right-align menu items in Ant Design


[reactjs - How to right-align menu items in Ant Design? - Stack Overflow](https://stackoverflow.com/questions/50882990/how-to-right-align-menu-items-in-ant-design "reactjs - How to right-align menu items in Ant Design? - Stack Overflow")


 

```html
<SubMenu style={{float: 'right'}} title={<span><Icon type="setting" />Navigation Three - Submenu</span>}>
      <MenuItemGroup title="Item 1">
        <Menu.Item key="setting:1">Option 1</Menu.Item>
        <Menu.Item key="setting:2">Option 2</Menu.Item>
      </MenuItemGroup>
      <MenuItemGroup title="Item 2">
        <Menu.Item key="setting:3">Option 3</Menu.Item>
        <Menu.Item key="setting:4">Option 4</Menu.Item>
      </MenuItemGroup>
    </SubMenu>
```
