# Lab Report 2 - Servers and Bugs (Week 3)
## Part 1 (String Server Implementation) 
Our goal is to write a web server called *String Server* which supports a
path behavior that allows users to add several lines of strings into the resulting web server.  
The parth request format will look like this: `/add-message?s=<string>`
<br> 
Here's the code/implementation <br>

![image](https://user-images.githubusercontent.com/122556045/215560636-7453aa7d-7ac0-48de-b16e-c7f1b3f9b089.png)

**The above image contains two classes (both of which extracted/derived from the week 2 lab) 
There are 2 methods, one in each class of the java file.** 
  - handleRequest (`public String handleRequest(URI url)`)
  - main method (`public static void main(String args[]`) 

### handleRequest 
- This method takes in a URI object titled url (
- When the main method runs, if the URI contains `/add-message` as part of the path, users can add strings after the = sign.  

### main 
- This method produces a link given a port number (which you include when running the code).  
- The link takes the user to a localhost site, where the above handleRequest method takes requests from the user given the right URI path

# Part 2 (Failure Inducing Inputs)
In the initial code of the `ArrayExamples` class, due to a bug in the `reverseInPlace` method,  
a failure inducing input includes trying to run the method on an array with 5 elements such as `[1,2,3,4,5]`    
Example: <br>
` @Test 
  public void testReverseInPlace2() { 
    int[] input = {1,2,3,4,5}; 
    ArrayExamples.reverseInPlace(input); 
    assertArrayEquals(new int[]{5,4,3,2,1}, input);
  } ` 
  <br> 
  On the contrary, a test that does not induce a failure is running the method on an array with only 1 element. 
  Example: <br> 
  `@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	} ` 
  ## Symptom 
  - Originally, we have a problematic symptom in the program, as an element in the array of 5 elements is incorrect 
  ![image](https://user-images.githubusercontent.com/122556045/215592237-8cb276ab-bfcd-4150-a5ca-28da8f08f688.png) 
  
  - Notice that we don't have this error for the array with only one element, this tells us that this method is problematic for arrays with several elements. This helps us in the debugging process. <br> 
 
 ![image](https://user-images.githubusercontent.com/122556045/215593598-22e1fc88-0d82-4b5a-b16a-8cf86fc0e6ca.png) (The test clearly passes) 
 
  ## The Bug
  - Upon further analysis, the issue with the code is that half way through the array, the elements will be set to the currently changed values of the earlier indexes. 
  - For instance, once the loop is at index 4, which is supposed to be changed to the **original** value of index 1 in an array with 5 elements, index 1 will have already been changed to the original index 4 value. Instead of a converstion from `[1,2,3,4,5] ----> [5,4,3,2,1]` as intended, you'll instead get a conversion of `[1,2,3,4,5] ------> [5,4,3,4,5]` 
  
  **Here's the original code.** <br>
  `// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {  
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }     
  }`
  
  ### Solution 
  One of many solutions is to declare a placeholder array thats the same size as the original, and copy all of the elements over in reverse order, and then copying the   elements from place holder back to the original array. 
  
  **Here is the fixed code** 
  ` // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {   
    int[] placeholder = new int[arr.length]; 
    
    for(int i = 0; i < arr.length; i += 1) {
      placeholder[i] = arr[arr.length - i - 1];
    }      

    for(int i=0; i<arr.length; i++){ 
      arr[i] = placeholder[i];
    } 
  }` 
  
  **This works because the original values are left in tact to copy to a temporary array, allowing for the final array to be properly reversed.** 
  
  # Part 3 (What I learned) 
  During this lab I learned 2 new things. 
  - How to copy github repositories onto the github desktop app (and even on VScode) 
  - how to commit changes via the terminal
  


