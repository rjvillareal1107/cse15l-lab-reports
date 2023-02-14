# Lab Report 3 

## Researching Commands: The grep Command 

The default grep command is used to print out all of the instances of a given string parameter within a single txt file.  
The syntax for grep is `grep [options] pattern [files]` (Source: [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/))

## Example of default command:  

![image](https://user-images.githubusercontent.com/122556045/218605198-c65c90b6-9c25-4512-9a5b-764aed3acc21.png) 

**(Quite the verbose image I know so allow me to explain)**  

This example uses the grep command to find instances of the word "Lucayans" in the file "Bahamas-History.txt"  

**(Notice that the target word is highlighted in red for easily visible reference.)** 

**As with many commands, grep has several different implementations and modifiers that allow the command to be used in all sorts of ways, we'll be exploring those in this lab report** 


## -r Modifier  

Typing -r after the grep command allows the computer to search every file in the working directory (including files within the associated subdirectories) for a given string pattern. This allows for several files to be searched at once. 

### Examples: 

#### Example 1: 

Input: 

![image](https://user-images.githubusercontent.com/122556045/218607774-3c65b8ff-d007-4ebb-9856-1e5681b880ca.png)


Result:

![image](https://user-images.githubusercontent.com/122556045/218606855-d576b66d-9c1d-403e-b88b-96b7c4d5a9ff.png) 

In the example above we are operating from the working directory ../skill-demo1-data. 
by using the command `grep -r "regional`, every single file under the working directory (including subdirectories) containing the target word "regional" is printed along with all of its contents


#### Example 2:  

Input: 

![image](https://user-images.githubusercontent.com/122556045/218608030-d5e1d6b3-71c2-4323-b523-8458ea67befa.png)


Result: 

![image](https://user-images.githubusercontent.com/122556045/218607463-8f8a3f86-4f30-47e5-864f-3e73b5b93b22.png) 

The same command was executed with the target word "congressional", as we can observe, there are even fewer files that contain this word.

#### How I found this command 

In the search for efficient terminal commands I've consulted my colleagues on what they know. 
I asked if there was a way to grep for a string pattern in all of the files in directory without first having to use the find command and redirect the output on a txt file to grep (which as implied takes significantly longer). The -r modifier was what was reccomended to me, which as a result streamlined the entire process of "grepping" for string patterns (Hurrah for valid peer collaboration) 

## -c pattern 

Let's say you are only concerned with the quantity of occurances of a single string pattern within a text file but nothing else. Using the grep command normally will print every occurance of the string pattern in the context of the file and if you want to find out the occurances of the pattern you'd have to count that individually. As one can imagine that would be beyond tedious.

**Fortunately there's a command that allows the user to simply display an integer representing the amount of occurances of a given string, this is the -c modifier. (Think of "c" as representative of the word count)** 

### Example 1: 

Lets say we want to determine the amount of times the word "Lucayans" appears in the file "Bahamas-History.txt". Here's what we'll do: 

Input:  

![image](https://user-images.githubusercontent.com/122556045/218611609-92a2daac-2870-40a2-a9fd-ff9c7dd1dd4b.png) 

Output: 

![image](https://user-images.githubusercontent.com/122556045/218611685-ee7d31cf-cc8c-4ad0-9aaa-e05b1ab3442d.png) 

**By using the -c command we are able to print the amount of occurances of the word "Lucayans" in the specified text file. 
In this case, it appears twice.** 

### Example 2: 

Let's say we want to list the number of occurances of the word "Lucayans" in every file in a directory, how do we do that? It can be achieved by combining the -r and -c commands upon calling grep. The syntax then would be `grep -rc <pattern>` 

Input:  

![image](https://user-images.githubusercontent.com/122556045/218612514-65f4ca1a-f80c-450c-be06-ba64aaf16b1f.png)


Output: 

![image](https://user-images.githubusercontent.com/122556045/218612710-73d406b6-7ab9-4308-a429-2cba195dd156.png)

As you see, combining these commands results in the terminal printing out the file names with the number of occurances next to each file name. With this we now know how many times "Lucayans" appears on every file under our working directory. Funny enough it only appears in 1 file (Bahamas-History.txt) twice :(. 

As specific as an implementation as this is, it is a testament to the variety of ways the grep command can be used. 

#### How I found this command 

the sight [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) has a list of several extensions for the grep command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax.

