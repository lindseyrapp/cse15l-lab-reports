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

**"Find" Command:** <br/>
I asked ChatGPT, "What are four different ways to use the find command in command line?" and learned several interesting uses for the find command. Here are 4 different methods of use, 2 examples for each:
<br/>

**Find File by Name:** <br/>

```
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find . -name "preface.txt"
./technical/911report/preface.txt
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find . -name "bcr317.txt"
./technical/biomed/bcr317.txt
```

<br/>

Here, we are searching for files by their names. It returns files that have names matching the input provided. (Found through ChatGPT, with prompt stated above)

<br/>

**Find Directory by Name:** <br/>

```
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find . -type d -name "911report"
./technical/911report
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find . -type d -name "biomed"
./technical/biomed
```

<br/>

Here, we are searching for directories by their names. It returns directories that have names matching the input provided. (Found through ChatGPT, with prompt stated above)

<br/>

**Find Directory by Type:** <br/>

```
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find ./ -type d
./
.//lib
.//.git
.//.git/objects
.//.git/objects/pack
.//.git/objects/info
.//.git/info
.//.git/logs
.//.git/logs/refs
.//.git/logs/refs/heads
.//.git/logs/refs/remotes
.//.git/logs/refs/remotes/origin
.//.git/logs/refs/remotes/upstream
.//.git/hooks
.//.git/refs
.//.git/refs/heads
.//.git/refs/tags
.//.git/refs/remotes
.//.git/refs/remotes/origin
.//.git/refs/remotes/upstream
.//.git/branches
.//technical
.//technical/government
.//technical/government/About_LSC
.//technical/government/Env_Prot_Agen
.//technical/government/Alcohol_Problems
.//technical/government/Gen_Account_Office
.//technical/government/Post_Rate_Comm
.//technical/government/Media
.//technical/plos
.//technical/biomed
.//technical/911report
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find ./technical -type d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```

<br/>

Here, we are searching by type. I used the command to search for directories by their type (-type d) with two different paths. It returns directories that are in the provided path. (Found through ChatGPT, with prompt stated above)

<br/>

**Find File by Size:** <br/>

```
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find ./technical/911report -type f -size -1M
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
(base) Lindseys-MacBook-Pro:docsssearch Linz$ find ./technical/911report -type f -size +100k
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-12.txt
```

<br/>

Here, we are searching for files by size. In the first example, I searched for all files with a size less than 1 megabyte. In the second example, I searched for files with a size greater than 100 kilobytes. (Found through ChatGPT, with prompt stated above)

<br/>


