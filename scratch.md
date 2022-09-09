### Task 1 (8 kyu)

You are given the length and width of a 4-sided polygon. The polygon can either be a rectangle or a square.
If it is a square, return its area. If it is a rectangle, return its perimeter.

Example(Input1, Input2 --> Output):

6, 10 --> 32

3, 3 --> 9

Note: for the purposes of this kata you will assume that it is a square if its length and width are equal, otherwise it
is a rectangle.

[Task link](https://www.codewars.com/kata/5ab6538b379d20ad880000ab/train/java)

#### Solution:

```Java
public class Solution {
    public static int areaOrPerimeter(int l, int w) {
        if (l == w) {
            return l * w;
        } else {
            return (l + w) * 2;
        }
    }
}
```

#### Fav solution:

```Java
class Solution {
    static int areaOrPerimeter(int l, int w) {
        return l == w ? l * w : 2 * (l + w);
    }
}
```

### Task 2 (8 kyu)

You are given two interior angles (in degrees) of a triangle.

Write a function to return the 3rd.

Note: only positive integers will be tested.

[Task link](https://www.codewars.com/kata/5a023c426975981341000014/train/java)

#### Solution:

```Java
public class ThirdAngle {
    public static int otherAngle(int a1, int a2) {
        return 180 - a1 - a2;
    }
}
```

#### Fav solution:

```Java
public class ThirdAngle {
    public static int otherAngle(int angle1, int angle2) {
        int angle3;
        if (angle1 < 0 || angle2 < 0) {
            System.out.println("Only positive integers!");
        }
        angle3 = 180 - (angle1 + angle2);
        if (angle3 < 0) {
            System.out.println("Impossible!");
        }
        return angle3;
    }
}
```