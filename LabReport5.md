# Lab Report 5: Lab that I liked  

<br> 

Over the course of the quarter I found that **Lab report 3** was the most useful on my end as it forced me to familiarize 
myself with terminal commands, which I believe to be an essential takeaway from this class. Last time we analyzed the `grep` command and took a deep dive into its versatility by analyzing some of grep's available extensions. This time, I aim to do the same for the `find` command and some of its most useful extensions. 

## Example of default command 

![image](https://user-images.githubusercontent.com/122556045/224853945-88f83e5a-0c99-425a-90ba-cf639a4c51f6.png)

Unlike the grep command, its arguable that the find command on its own doesn't have that much functionality, as it displays all of the 
subdirectories and files in the given directory, which isn't that useful. This means the importance of understanding the available extensions 

## Extension 1: Directory modifier 

You can actually specify the directory you would like to view files in. We do this by specifiying the directory right after the find 
command 

### Example 1: 

![image](https://user-images.githubusercontent.com/122556045/224855101-50195405-6559-4b0a-a234-a2a9b8dda456.png)

In the example above I used `find .` to specifically search my current directory. 

### Example 2: 

![image](https://user-images.githubusercontent.com/122556045/224855386-af97f527-0a03-42f3-8dcf-422d387f3b89.png) 

In this example, we used `find ./lab7` to specifically view everything under the `lab7` directory.  

#### How I found this command 

The site [geeksforgeeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) has a list of several extensions for the find command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax. 

## Extension 2: -type extension 

After specifying the directory, you can use the `-type` extension followed by a specific character to view all 
files of a specific type, this includes directories, files, symlinks, etc. 

### Example 1:

![image](https://user-images.githubusercontent.com/122556045/224856402-958043c2-3585-4795-8ba3-64038b1f6ebe.png) 

In this example I used `-type f` in the current directory to view everything that is considered a file 

### Example 2: 

![image](https://user-images.githubusercontent.com/122556045/224856524-9a2995a1-5df0-4462-8973-550167558537.png) 

In this example I used `-type d` in the current directory to view everything that is consideered a subdirectory. 

#### How I found this command  

The site [geeksforgeeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) has a list of several extensions for the find command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax. 

## Extension 3: -name extension 

The name extension allows us to find out the subdirectory name of a given file. 

### Example 1: 

![image](https://user-images.githubusercontent.com/122556045/224857273-0f84e462-da1f-45c2-b774-9600d55cb812.png) 

In this example, we used  `-name ListExamples.java` to get the subdirectory name of the file `ListExamples.java`. 

### Example 2: 

![image](https://user-images.githubusercontent.com/122556045/224857569-eceb40a8-def6-40a7-9c83-d1a03135729c.png) 

In this example we used `-name ListExamplesTests.java` to get the subdirectory name of the file `ListExamplesTests.java` 

#### How I found this command   

The site [geeksforgeeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) has a list of several extensions for the find command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax. 

## Extension 4: Pattern Recognition 

This is really an extenstion to the name extension and works similarly to  `-type` but can be applied to specific types of files. 
You simply type a text file pattern after `-name` (EX: *.txt) and all files of that type will appear as the system checks for the specified pattern. "*" Is a placeholder for all possible file names with everything after being the specified pattern. 

### Example 1: 

![image](https://user-images.githubusercontent.com/122556045/224858997-6fa68848-21b0-43ea-a30c-98e2c0b54661.png) 

In this example I used the `*.txt` pattern to have the terminal display all `.txt` files in the current working directory. 

## Example 2: 

![image](https://user-images.githubusercontent.com/122556045/224859150-f4dfc5e7-1e3a-4847-bea3-2ba2057a481a.png)

In this example I used the `*.class` pattern to have the terminal display all `.class` files in the current working directory.  

#### How I found this command   

The site [geeksforgeeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) has a list of several extensions for the find command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax. 


## Summary 

Similar to grep, the find command is made versatile by the use of extensions, which operate in a variety of different ways.

