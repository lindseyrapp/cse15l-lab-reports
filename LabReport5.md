# Lab Report 5 by Lindsey Rappaport
## *Week 9 - Putting It All Together*
## CS 15L

## **Part 1:** <br/>
**EdStem Question:** <br/> <br/>
![Image](edStemQ.png) <br/>
This is the question posted on edStem with the failure-inducing input and symptom.
<br/>
<br/>
**EdStem TA Response:** <br/>
![Image](edStemA.png) <br/>
This is the response from the "TA" with a suggestion on commands to run to identify the bug.
<br/>
<br/>
**Trying Out the Suggestions:** <br/>
![Image](firstTry.png) <br/>
Here, I followed the TA's advice and entered two even integers as input. It returned the correct average. Because of this result, I ran the cat command to inspect the code and found that the TA's prediction was correct: the return type was incorrect for the findAvg function.
<br/>
<br/>
![Image](vimFix.png) <br/>
Here, as suggested, I used vim to fix the code. I entered insert mode and changed the return type for findAvg. I also changed the "2" to "2.0" in the equation to be consistent with doubles.
<br/>
<br/>
![Image](fixed.png) <br/>
Here, I ran the bash script with the new and improved code. I entered the same integers that originally caused failure, and the code returned the correct value this time.
<br/>
<br/>
**Necessary Information:** <br/>
![Image](codeVS.png) <br/>
This was the code in AverageCalculator.java **BEFORE** the bug was fixed. This file was stored in the Desktop directory on my computer.
<br/>
<br/>
![Image](bash.png) <br/>
This was the contents of the bash script, which did not change throughout the process. This file was stored in the Desktop directory on my computer.
<br/>
<br/>
![Image](symptom.png) <br/>
Here is the full command line that was run to produce the original symptom. 
<br/>
<br/>
How I fixed it: To fix the bug, I changed the return type from int to double for the findAvg function. I also changed the 2 in the equation to 2.0.


## **Part 2:** <br/>
In the second half of the quarter for this lab, I learned a lot about command line tools and ways to make identifying bugs easier. Something specific I learned was the wc command. I have used the command line a lot before for my job, but have never had to use this command. I like that it counts words, lines, and characters. This could be useful in the future so I was happy to learn about it. I also learned different ways to utilize vim. I have used it with the insert mode, but I had not previously used the shortcuts like replace, delete, etc. This can make editing files easier for sure.
