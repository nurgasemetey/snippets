###  null comparator java 


[java - comparator with null values - Stack Overflow](https://stackoverflow.com/questions/2401606/comparator-with-null-values "java - comparator with null values - Stack Overflow")


 

```
comp(1234, null) == -1
comp(null, null) == 0
comp(null, 1234) == 1



if (o1.getBiddingDepartment() == null && o2.getBiddingDepartment() == null ) {
			return 0;
		}
		else if (o1.getBiddingDepartment() == null) {
			return -1;
		}
		else if (o2.getBiddingDepartment() == null) {
			return 1;
		}
```
