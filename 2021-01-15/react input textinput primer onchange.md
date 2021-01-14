### react input textinput primer onchange


[javascript - How to get the value of an input field using ReactJS? - Stack Overflow](https://stackoverflow.com/questions/36683770/how-to-get-the-value-of-an-input-field-using-reactjs "javascript - How to get the value of an input field using ReactJS? - Stack Overflow")



[gh-users-explorer/SearchInputView.jsx at 244e6659d4d33dcab8139a4af32fa15dfb3d7372 · PiotrAleksander/gh-users-explorer](https://github.com/PiotrAleksander/gh-users-explorer/blob/244e6659d4d33dcab8139a4af32fa15dfb3d7372/src/components/views/SearchInputView.jsx "gh-users-explorer/SearchInputView.jsx at 244e6659d4d33dcab8139a4af32fa15dfb3d7372 · PiotrAleksander/gh-users-explorer")


 

```
updateInput(event){
this.setState({username : event.target.value})
}

  <TextInput
    onChange={(event) => {
      event.persist();
      onChange(event);
    }}
    ml={4}
    icon={SearchIcon}
    aria-label="organization"
    name="organization"
    placeholder="Find an organization"
  />
```
