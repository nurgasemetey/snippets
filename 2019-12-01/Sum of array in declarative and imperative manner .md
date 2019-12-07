### Sum of array in declarative and imperative manner 





 

```java
public class SumArrayImperative implements SumArray {
    @Override
    public long sum(int[] arr) {
        long sum = 0;
        for (int i : arr) {
            sum += i;
        }
        return sum;
    }
}


import java.util.stream.IntStream;

public class SumArrayDeclarative implements SumArray {

    @Override
    public long sum(int[] arr) {
        return IntStream.of(arr)
                .mapToLong(i -> i)
                .sum();
    }
}

```
