# Lab Report 4 - CSE Labs "Done Quick" 

<br> For our lab, we were tasked with cloning, editing, and commiting files from a github fork, and speeding up the process 
as much as we can. here is a detailed report of all of the steps that I took (specifically steps 4-9) 

## Step 4 "Log into ieng6" 

<br> This step simply involves logging into ieng6 with the appropriate user name and password 

**Screenshot** 

![image](https://user-images.githubusercontent.com/122556045/224843291-a20d5e11-fa29-4c74-bbbd-f64fefecefd9.png) 

Keys pressed: <ssh cs15lwi23aeq@ieng6.ucsd.edu> -------> <*password*> 

Summary: <br> 

This connects me to my ieng6 account by having myself verify my username and associated password 

## Step 5 "Clone the fork from the repository onto your github account" 

We need to clone the repository in order to have access to and edit the files we need 

**Screenshot**

![image](https://user-images.githubusercontent.com/122556045/224845085-00854cb8-0eab-414b-acb1-8e5cfa4f2e88.png)

keys pressed: <git> <clone> <https://github.com/rjvillareal1107/lab7.git> (the repository link is copy pasted) 
  
Summary: <br> 

This creates a copy of the repository in our current directory 
  
## Step 6 "Run Tests, demonstrating that they fail" 

Our goal with these steps is to compile and run the provided Junit tests. 

**Screenshot**  
  
![image](https://user-images.githubusercontent.com/122556045/224846744-22fda0de-95b0-4f20-87bd-1895aab40107.png) 
  
keys pressed: 
  
              <cd lab7> <javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java> (Copy pasted) 
              <java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore List
              ExamplesTests> (copy pasted) 
                
Summary: <br> 

I changed my directory to lab7, and then compiled and ran the Junit tests. As the writeup specifies, the tests fail 
indicating that there is something wrong with the code.

  
