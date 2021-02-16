### python division python 2 python 3


[Python integer division yields float - Stack Overflow](https://stackoverflow.com/questions/1282945/python-integer-division-yields-float "Python integer division yields float - Stack Overflow")


 

```
Behavior of Division Operator in Python 2.7 and Python 3
In Python 2.7: By default, division operator will return integer output.

to get the result in double multiple 1.0 to "dividend or divisor"

100/35 => 2 #(Expected is 2.857142857142857)
(100*1.0)/35 => 2.857142857142857
100/(35*1.0) => 2.857142857142857
In Python 3

// => used for integer output
/ => used for double output

100/35 => 2.857142857142857
100//35 => 2
100.//35 => 2.0    # floating-point result if divsor or dividend real
```
