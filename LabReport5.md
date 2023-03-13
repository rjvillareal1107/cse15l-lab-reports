# Lab Report 5: Lab that I liked  

<br> 

Over the course of the quarter I found that Lab report 3 was the most useful on my end as it forced me to familiarize 
myself with terminal commands, which I believe to be an essential takeaway from this class. Last time we analyzed the grep command 
and a few of its modifications, this time, I aim to do the same for the **find** command. 

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
files of a specific type, this includes directories, files,
