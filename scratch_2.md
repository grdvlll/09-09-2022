### Task 1 (8 kyu)

You will be given an array a and a value x. All you need to do is check whether the provided array contains the value.

Array can contain numbers or strings. X can be either.

Return true if the array contains the value, false if not.

[Task link](https://www.codewars.com/kata/57cc975ed542d3148f00015b/train/java)

#### Solution:

```Java
public class Solution {

    public static boolean check(Object[] a, Object x) {
        for (int i = 0; i < a.length; i++) {
            if (a[i] == x)
                return true;
        }
        return false;
    }

}
```

#### Fav solution:

```Java
public class Solution {

    public static boolean check(Object[] a, Object x) {
        return Arrays.asList(a).contains(x);
    }

}
```

### Task 2 (7 kyu)

Implement a function that accepts 3 integer values a, b, c. The function should return true if a triangle can be built with the sides of given length and false in any other case.

(In this case, all triangles must have surface greater than 0 to be accepted).

[Task link](https://www.codewars.com/kata/56606694ec01347ce800001b)

#### Solution:

```Java
class TriangleTester{
    public static boolean isTriangle(int a, int b, int c){
        if ((a + b > c) && (a + c > b) && (b + c > a))
            return true;
        else
            return false;
    }
}
```

#### Fav solution:

```Java
class TriangleTester{
    public static boolean isTriangle(int a, int b, int c){
        return a + b > c && a + c > b && c + b > a;
    }
}
```