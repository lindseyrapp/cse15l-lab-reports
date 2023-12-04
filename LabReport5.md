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
**Path to Private Key:** <br/>
![Image](privPath.png) <br/>
**Path to Public Key:** <br/>
![Image](pubPath.png) <br/>
**Successful Login with no Password:** <br/>
![Image](successNoPW.png) <br/>

## **Part 3:** <br/>
During weeks 2 and 3, I learned about using methods in servers to edit files using the search bar, which I have never done before. I also learned about the use of private and public keys to gain access to remote servers without having to use a password each time which is very useful.
<br/>
