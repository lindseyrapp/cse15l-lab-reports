# Lab Report 4 by Lindsey Rappaport

## *Week 7 - Vim*

## CS 15L

## **Part 1-Bugs:** <br/>

**Failure Inducing Input in Test:** <br/>

```
public void testReverseInPlace() {
    int[] input1 = {3,1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1,3}, input1);
  }
```

<br/>

