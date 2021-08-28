### java add elements during iteration


[java - Adding elements to a collection during iteration - Stack Overflow](https://stackoverflow.com/questions/993025/adding-elements-to-a-collection-during-iteration "java - Adding elements to a collection during iteration - Stack Overflow")


 

```
Queue<Integer> queue = new LinkedList<Integer>();
queue.add(1);
queue.add(2);
queue.add(3);
queue.add(4);

while (!queue.isEmpty()) {
    Integer i = queue.remove();
    if (i == 2)
        queue.add(42);

    System.out.println(i);
}
```
