# 09-09-2022
### Task 1 (8 kyu)


You are given an array with positive numbers and a non-negative number N. You should find the N-th power of the element in the array with the index N. If N is outside of the array, then return -1. Don't forget that the first element has the index 0.

Let's look at a few examples:

array = [1, 2, 3, 4] and N = 2, then the result is 3^2 == 9;

array = [1, 2, 3] and N = 3, but N is outside of the array, so the result is -1.

[Task link](https://www.codewars.com/kata/57d814e4950d8489720008db/train/java)
#### Solution:
```Java
public class Kata {
  public static int nthPower(int[] arr, int N) {
    int res;
    if (arr.length > N){
      res = (int) Math.pow (arr[N], N);
    }
    else{
      res = -1;
    }
    return res;
  }
}

```

#### Fav solution:
```Java
public class Kata {
  public static int nthPower(int[] array, int n) {
    for (int i = 0; i < array.length; i++) {
      if (i == n) {
        return (int) Math.pow(array[i], n);
      }
    }
    
    return -1;
  }
}
```

### Task 2 (8 kyu)

Write a method, that will get an integer array as parameter and will process every number from this array.

Return a new array with processing every number of the input-array like this:

If the number has an integer square root, take this, otherwise square the number.

Example:
[4,3,9,7,2,1] -> [2,9,3,49,4,1]

Notes:

The input array will always contain only positive number s, and will never be empty or null.

[Task link](https://www.codewars.com/kata/57f6ad55cca6e045d2000627)

#### Solution:
```Java
public class Kata
{
  public static int[] squareOrSquareRoot(int[] array)
  {
    int[] array_1 = new int[array.length]; 
    for (int i = 0; i < array.length; i++){
      if (Math.sqrt(array[i]) % 1 == 0){
        array_1[i] = (int) Math.sqrt (array[i]);
      }
      else{
        array_1[i] = (int) Math.pow (array[i], 2);
      }                       
    }
    return array_1;
  }
}
```

#### Fav solution:
```Java
public class Kata
{
  public static int[] squareOrSquareRoot(int[] array)
  {
    for(int i = 0; i < array.length; i++) {
      if (Math.sqrt(array[i]) % 1 == 0) array[i] = (int) Math.sqrt(array[i]);
      else array[i] = array[i] * array[i];
    }
    return array;
  }
}
```
