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
                
## Step 7 "Edit the code to fix the failing test"  
 
Upon inspection of the file in Github, it appears that the problem is that in line 43, index1 is incremented and not index2. 
To fix this, we will use nano to manually edit the code, and recompile the class file. 

**Screenshot** 

![image](https://user-images.githubusercontent.com/122556045/224848348-1e187c7a-72a6-419c-92a5-dcde4fa0896e.png) 
![image](https://user-images.githubusercontent.com/122556045/224848421-e4177196-58bf-47dd-a826-de3903fc22e1.png) 
![image](https://user-images.githubusercontent.com/122556045/224848522-0175cf76-cd46-413c-8d5a-7cede390a988.png)


keys pressed: 
               
               <nano ListExamples.java> <CTRL^W "while(index2 <list2.size())"> <down> <down> <down> <down> <down> <down> 
               <right> <right> <right> <right> <right> <right> <right> <right> <right> <backspace> <2> <CTRL^o> <enter> 
               <javac List> <tab> <.j> <tab> 
                 
Summary: <br> 

On top of regular commands, I used a few shortcuts to speed up the process. First I typed "nano ListExamples.java". This allows 
me to use nano to edit the java file. once the editor opens up we use the seach command CTRL^W and type a line close to what we want to edit so we don't need to press the down key over and over. Follwing this we use the arrow keys to navigate to the code we want to change, change it, then use CTRL^o to save our changes. After this we recompile the class file so that our changes are applicable.         
                 
## Step 8: "Run the tests, demonstrating that they now succeed"       

With our code fixed, we need to run the tests to see if they passed.    
                 
**Screenshot** 

![image](https://user-images.githubusercontent.com/122556045/224850508-8eb56d55-5552-4572-8041-a2013976a280.png)

keys pressed: 
                 
                 <up> <up> <up> <up> <enter> 
                
Summary: <br> 
                 
Similar to the previous step, we used available keyboard shortcuts to speed up the process. We pressed up to see our previous commands until we got to the command which allows us to view the command which lets us run the JUNit tests, all we needed to do from there is press enter and the tests run, passing this times around.     
                 
## Step 9 "Commit and push the resulting change to your Github account" 
                   
The last step is to add, commit, and push our changes.  
                   
 **Screenshot** 
                   
 ![image](https://user-images.githubusercontent.com/122556045/224851505-0908cbd9-8ced-4fab-bb1e-d52f36e9755d.png)

 keys pressed: 
                   
                   <git add L> <tab> <.j> <tab> <enter> <git commmit -m "finished"> <enter> <git push> <enter> 
                     
 Summary: <br> 
 
 I used the established git commands to add, using tab to autocomplete the file name. I commited my changes with the message "finished", and then used the git push command to finalize and push my changes to the main repository branch.
                     
