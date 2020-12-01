###  antd cell colour table


[reactjs - How can i change the cell colour in ANTD table according to the value? - Stack Overflow](https://stackoverflow.com/questions/59100322/how-can-i-change-the-cell-colour-in-antd-table-according-to-the-value "reactjs - How can i change the cell colour in ANTD table according to the value? - Stack Overflow")


 

```
 columns: [
      {
        title: "Date",
        dataIndex: "date",
        width: 200
      },
      {
        title: "Amount",
        dataIndex: "amount",
        width: 100,
        render(text, record) {
          return {
            props: {
              style: { background: parseInt(text) > 50 ? "red" : "green" }
            },
            children: <div>{text}</div>
          };
        }
      },
      {
        title: "Type",
        dataIndex: "type",
        width: 100
      },
      {
        title: "Note",
        dataIndex: "note",
        width: 100
      }
    ]
```
