###  [Task 7kyu](https://www.codewars.com/kata/58aed2cafab8faca1d000e20/train/java)



You are provided with an array of positive integers and an additional integer n (n > 1).

Calculate the sum of each value in the array to the nth power. Then subtract the sum of the original array.





### My solution
```Java
import java.io.*;
public class Kata {
    public static int modifiedSum(int[] array, int power) {
        int sum1 = 0;
        int sum2 = 0;
        for(int i = 0; i < array.length; i++){
            sum1 += Math. pow(array[i], power);
            sum2 += array[i];
        }
        return sum1-sum2;
    }
}
```

### Fav solution

```Java
import java.util.stream.IntStream;

public class Kata {
    public static int modifiedSum(int[] array, int power) {
        return IntStream.of(array).map((base) -> (int) Math.pow(base, power) - base).sum();
    }
}
 

```
I like this solution because I like it
