# Week 4 Lab Report
**What we did:** In this lab report, I'll talk about 
three code changes that our group worked on in Lab 3
 and Lab 4 in order to fix a bug in the MarkdownParse.
 java.
 
## First Code Change
**1. Screenshot of the code change**

Here is the screenshot of the code change difference from Github. In this 
file, we basically added a few lines of an if statement (from line 22 to line 24) which makes
a difference from the origin code.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/code1.png)

**2. Link to the test file**

Here is the [test2.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test2.md)
for a failure-inducing input that prompted us to make that change above. 
We created a new test2.md which includes two pseudo links (a website link 
and an image link). However, we don't really want the image link in our output.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/test1.png)

**3. The symptom of failure-inducing input**

Here is the output of running the file at the command line for the version where it was failing. 

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/symptom1.png)

>the relationship between the bug, the symptom, and the failure-inducing input.

The bug in the code is that we didn't have lines of code to restrict when to add new links to
 toReturn arraylist. The bug causes the symptom to appear when we run the command. Therefore, we 
 saw the symptom that the output gives us the image link in 
 [test2.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test2.md), and we don't really want 
 the image link to be printed. We were able to find the bug and see the symptom because we decided
  to include an image link in the [test2.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test2.md)
  , which is the failure-inducing input. It becomes the 
  breaking point of the program so we were able to make some changes to the code.

<br/>

## Second Code Change

**1. Screenshot of the code change**

Here is the screenshot of the code change difference from Github. This time, we added another condition 
for the if statement in the code.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/code2.png)

**2. Link to the test file**

Here is the [test4.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test4.md) 
for a failure-inducing input that prompted us to make the change. In this test, we added 
an invalid line so we expected nothing to be printed out when we ran the code. 

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/test2.png)

**3. The symptom of failure-inducing input**

Here is the output of running the file at the command line for the version where it was failing.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/symptom2.png)

>the relationship between the bug, the symptom, and the failure-inducing input.

The bug in this code is that we didn't have a line to check whether it is a valid line of link in 
the code. Because of this bug, we saw the symptom that it still gave us the link even though it 
should not print anything because there's no valid link in the 
[test4.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test4.md). The failure-inducing 
input, adding an invalid line of link in the test file, allowed us to see the symptom when we ran the command 
and fixed the bug by adding another condition to the if statement to avoid printing anything when it's a invalid
 link.

<br/>

## Third Code Change

**1. Screenshot of the code change**

Here is the screenshot of the code change difference from Github.


![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/code3.png)

**2. Link to the test file**

Here is the [test5.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test5.md) 
for a failure-inducing input that prompted us to make that change. 
In this test, we put a word inside the parenthesis which is not an actual link, 
so we expected that it should not give us any link when we ran the command.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/test3.png)

**3. The Symptom of that failure-induing input**

Here is the output of running the file at the command line for the version where it was failing.

![Image](https://github.com/CATHCHEN014/markdown-parse/blob/main/symptom3.png)

>the relationship between the bug, the symptom, and the failure-inducing input.

The bug in the code is that we didn't check whether it is an actual link inside the parenthesis. It could 
be a full sentence or some random words inside the parenthesis and this is not an actual link so it should 
not be printed when we run the command. However, since we didn't have this condition in our if statement before, 
the code could not tell whether it could be an actual link or not. Therefore, we saw the symptom that it still 
prints out the content inside the parenthesis even though it is not a link. The failure-inducing input, adding some 
random words (not an actual link) in the [test5.md](https://github.com/CATHCHEN014/markdown-parse/blob/main/test5.md), 
so we could see the breaking point of the program so we could fix it.

<br/>

### By Catherine Chen

### 1/27/2022
