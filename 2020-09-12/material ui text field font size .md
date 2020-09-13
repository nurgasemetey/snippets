### material ui text field font size 


[css - Cannot change font size of text field in material ui - Stack Overflow](https://stackoverflow.com/questions/50319847/cannot-change-font-size-of-text-field-in-material-ui "css - Cannot change font size of text field in material ui - Stack Overflow")


 

```
const styles = {
container: {
    display: 'flex',
    flexWrap: 'wrap',
},
textField: {
    width: 300,
    margin: 100,
},
//style for font size
resize:{
  fontSize:50
},
}

<TextField 
                          InputProps={{
                            classes: {
                              input: classes.resize,
                            },
                          }} 
                          fullWidth 
                          // size="medium"
                          />
```
