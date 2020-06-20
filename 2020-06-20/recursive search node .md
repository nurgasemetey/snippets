### recursive search node 


[java - Recursive search for a node in non-binary tree - Stack Overflow](https://stackoverflow.com/questions/8617790/recursive-search-for-a-node-in-non-binary-tree "java - Recursive search for a node in non-binary tree - Stack Overflow")


 

```java
private nNode recursiveSearch(data gi,nNode node){
        if (node.getdata()==gi)
            return node;
        nNode[] children = node.getChildren(); 
        nNode temp;
        if (children.length>0)
        for (int i = 0; i < children.length; i++) {         
            temp = recursiveSearch(gi, children[i]);
            if(temp!=null)
                return temp;
        }
        return null;
 }
```
