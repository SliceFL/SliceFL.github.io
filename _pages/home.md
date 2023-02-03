---

permalink: /home/
title: "Homepage of the SliceFL project"
author_profile: true
toc: true
toc_label: "Content"
toc_icon: "cog"
---

## The fate of the developer

As we know well since Murphy, *what can go wrong, will go wrong*. This applies to software programs as well, and finding bugs can be a challenging and time-consuming task, not to mention that fixing one issue often leads to the discovery of several others. Over the years, various automated methods have been developed to tackle this problem, such as coverage-based SBFL and program slicing. However, these methods are more theoretical than practical, as the former is fast but inaccurate, while the latter is accurate but too expensive to use.

## The Slice-FL appears

With the Slice-Fl project, we aim to have an automatic debugging method that can effectively help developers in real-world situations. To this end, we combine classical SBFL and dynamic backward slicing, exploiting the positive features of both while minimizing their drawbacks. We achieve this by replacing the hit-based coverage matrix with a slicing basis, i.e., starting from the assert statements in the tests, we compute the sets of statements that affect the assert's output. The advantage of this method is, among others, that the slice, since it does not contain instructions whose execution is irrelevant to the result, leads to a smaller and more accurate matrix.

### Example

Here we present a short example that emphasize the usefulness of our approach.
In this example, the first code snippet contains a Circle class with some basic operations. The error is in the constructor when calculating the perimeter (a multiplier of two is missing). 
```java
public class Circle {
    private double area;
    private double perimeter;
    public Circle(double radius) {
        area = radius * radius * Math.PI;
        perimeter = radius * Math.PI; // faulty statement
    }
    double getArea() {
        return area;
    }
    double getPerimeter() {
        return perimeter;
    }
}
```
The second code snippet shows how to test the Circle class. If these tests are run, t2 will report an error, however, tests t1 and t3 will pass. This is a problem because t3 covers the faulty statement in the constructor and nevertheless does not fail, i.e. it will distort the suspiciousness value associated with the given row (i.e. the perimeter calculation) (you can see that it, along with several others, has a value of 0.5).

```java
import junit.framework.TestCase;

public class CircleTest extends TestCase {
	 static Circle circle = new Circle(0);
    public void t1() {
        assertEquals(Math.PI, new Circle(1).getArea(), 1e-10);
    }
    public void t2() {
        assertEquals(2.0*Math.PI, new Circle(1).getPerimeter(), 1e-10);
    }
    public void t3() {
        assertEquals(0, circle.getPerimeter(), 1e-10);
    }
}
```

In contrast, with the slicing approach (as shown in the second table), it is clearly the faulty row that already gets the highest value. The reason for this is that the Kör object used here has already been created, so when the slice is calculated, the instructions in it will not be rerun and therefore will not be included in the slice (unlike the second test, where a new object is used).
![coverage](/assets/images/coverage.png)

![slice](/assets/images/slice.png)
