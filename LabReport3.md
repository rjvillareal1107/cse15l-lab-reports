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

## -c Modifier 

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

The site [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) has a list of several extensions for the grep command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax. 

## -n Modifier 

### Example 1 

The -n Modifier allows the matched lines with the target string pattern to be highlighted, as well as the specific line that the word appears in. 

Input: 

![image](https://user-images.githubusercontent.com/122556045/218664450-5672c2cc-49c9-410a-956b-d34ab67ba6cc.png) 

Output: 

![image](https://user-images.githubusercontent.com/122556045/218664543-3037ed20-b2e2-4dff-90e6-08aca8e73e1b.png)

As you can see, not only is the target string highlighted, but in addition to that, the terminal highlights the line number in which the target string is found. 

**Note: In this case, we combined the -n command with the -r command to do this with multiple files by searching for all associated files recursively. However the -n command can be done alone on a single text file.**

### Example 2: 

We can use the n command on a single text file. 

Input: 

![image](https://user-images.githubusercontent.com/122556045/218665177-10c959ed-bec3-4900-b40c-1d925221d042.png)

Output: 

![image](https://user-images.githubusercontent.com/122556045/218665284-0f08d0a7-519c-49e6-95bb-708c1ed2a48d.png) 

This shows us all of the lines with "Lucayans" in the text file, including their line numbers. 

#### How did I find this command

The site [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) has a list of several extensions for the grep command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax.  

## The -o Modifier 

In all of the examples, when matching a text file with a given phrase, the target string is highlighted, but all of the text within the file is printed as well, making for a very cluttered screen full of possibly unnecesary/uneeded information. The -o modifier allows us to print only the matched parts of the txt file.

### Example 1: 

We can print exclusively the matching parts in a single .txt file 

Input: 

![image](https://user-images.githubusercontent.com/122556045/218666931-7232c821-f1dc-45b7-8ab8-1d8024e19d1e.png)
 
 
 Output: 
 
 ![image](https://user-images.githubusercontent.com/122556045/218666975-fed1652a-b32f-4e5e-97c6-ce4bc7a81f84.png) 
 
 
 As shown above, only the matching lines appear. 
 
 ### Example 2: 
 
 We can do the same command but to multiple files at once by combining modifiers. 
 
 Input: 
 
 ![image](https://user-images.githubusercontent.com/122556045/218667454-dcd1dd5d-3302-49b1-9d53-55d65dc5126c.png)
 
 Output: 
 
 ![image](https://user-images.githubusercontent.com/122556045/218667572-526795a7-6816-40ee-abab-e7d93d258bef.png) 
 
 Combining the -r and -o modifiers prints the matching parts from all applicable files in the given directory.  
 
 #### How did I find this command 
 
 The site [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) has a list of several extensions for the grep command complete with descriptions and even some examples. This is useful not only for finding out what commands are available, but also as reference for possible applications and syntax.   
 
 # Conclusion 
 
 Studying the grep command helped me find a wide range of applications for the command. 
 -r allows grep to be used on all of the files in the directory, allowing potentially hundreds of files to be searched simultaneously 
 -c allows us to find out the amount of times a given phrase is used. 
 -n allows us to display the matched lines along side which numbered line the phrase is on 
 and -o allows us to print only the matched sections. 
 
 It's also worth noting that the ability to combine these commands opens up the possibility for several more applications, which heavily increases the overall utility 
 of the grep command. 
 
 Overall, this exersize has stressed the potential that command modifiers have.

 
 
 
