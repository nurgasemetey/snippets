###  antd tree title style render


[Tree - Ant Design](https://ant.design/components/tree/ "Tree - Ant Design")


 

```
            <DirectoryTree
              // style={{
              //   lineHeight:5
              // }}
              onSelect={onSelect}
              onExpand={onExpand}
              treeData={treeData}
              defaultSelectedKeys={[treeData[treeData.length - 1].key]}
              titleRender={(nodeData: any) => {
                // console.log(nodeData);
                return (<Text style={{ fontSize: 16, margin: 5 }}>{nodeData.title}</Text>)
              }}
            />
```
