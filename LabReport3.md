# Lab Report 3 by Lindsey Rappaport

## *Week 5 - Bugs and Commands*

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

**Input that does not Induce Failure in Test:** <br/>

```
public void testReverseInPlace() {
    int[] input1 = {3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3}, input1);
  }
```

<br/>

**Symptom:** <br/>

**With Failure Inducing Input:** <br/>

![Image](failInduce.png) <br/>

**With Input that does not Induce Failure:** <br/>

![Image](noFail.png) <br/>

**Code Before Fix:** <br/>

```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

<br/>

**Code After Fix:** <br/>

```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length-i-1] = temp;
    }
  }
```

<br/>
The original code failed because it tried to reverse the array by copying values from the end all the way to the beginning. Because of this, elements were overwritten, & the array produced was not reversed as desired.
The updated method fixed this by iterating up to half of the array's length & creating a temporary array to store values. During each iteration, the new method swaps the elements from the beginning and the end of the array. Because “temp” was created, no values were overwritten like before, so it works as desired.
<br/>

## **Part 2-Researching Commands:** <br/>
**Path to Private Key:** <br/>
![Image](privPath.png) <br/>
**Path to Public Key:** <br/>
![Image](pubPath.png) <br/>
**Successful Login with no Password:** <br/>
![Image](successNoPW.png) <br/>

