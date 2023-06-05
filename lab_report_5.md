#  Lab Report 4

Hello! Welcome to the final part of your CS15L Journey. It has truly been an interesting quarter.

## Debugging Scenario

![Image](Debugging.jpg.png)

**What Environment are you using?**

I am using Visual Studios Code and am using Linux to run my terminal on my Mac computer. I keep getting this Junit error when I try to run my test and I am unsure why.

**Detail the symptoms you are seeing**

The symptoms I am seeing is that the terminal cannot find the file I am entering in the command line, even though I wrote it exactly as it appears on the left and top of my screen. I have checked the rest of my code and it works fine. I double checked by running it by Chat GPT to see if there are any errors I might have missed.  

**Detail the failure inducing input and context. That might mean any or all the commands you are running, a test case, command line arguments, or working directory**

The command line I am putting in is what is on the lab assignment, the only thing I had to do was add the file I want to run in my Junit test. I have checked that I am in the correct directory and that my code compiles. When I run the code outside of the Junit test it works fine.

**Response**

TA: Hi Grace, from what I can see it looks like all of your code is correct. The problem is with your command line. If you look in the command line at the line that says IllegalArgument ... at the end it says that it could not find 'ArrayTests.java'. This is because we need to write different parts of the file name when we are compiling code compared to running code. When we compile code we want to include  'Arraytests.java' and when we run code we do not want to include the .java. Try running the same command line
