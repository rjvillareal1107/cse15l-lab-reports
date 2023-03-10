# Lab Report 1  
By: Robin Villareal  

Here's a quick tutorial on how to get started with CSE15L. Steps include: 
* Installing Vscode 
* Connecting to the public CSE15L server (CSE Basement)
* Trying some commands 

# Downloading VScode <br> 
VScode will serve as the primary IDE for this class, and we'll use it to input a variety of terminal commands later. 

- First, download VSCode online [VScode link](https://code.visualstudio.com/)
- Then, follow the instructions of the installer. 
- When you open VScode, it should take you to a welcome menu not unlike the image below, you can now open files, access terminals, and edit code. 

![image](https://user-images.githubusercontent.com/122556045/212161562-0921030f-dd6f-4a29-bdc2-da13d98b6ce1.png) 

***Important!!!** If not done already, install Java on your device!*  

# Connecting to the CSE Basement server <br> 
There are essentially 3 steps in this process, which include downloading git, activating your CSE15L account, and finally logging in.

## How to install git 
- go to [Git Install Link](https://gitforwindows.org/) 
- download and follow the instructions of the installer 
- After installation, the Git BASH terminal should be available in VScode, under terminal options 

![image](https://user-images.githubusercontent.com/122556045/212165742-8378faf3-fb48-4bf9-9756-3d5d88c36d03.png)  
(You can use both the powershell and gitBASH terminals for this activity, but it is important to have gitBASH installed)

## Activating your CSE15L account 
Your CSE15L account needs to be properly activated in order to succesfully log in. 
- First go to [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) 
- Log in with your UCSD credentials. 
![image](https://user-images.githubusercontent.com/122556045/212212541-54a06c3f-4bce-43dc-9cb1-072fc61569c0.png) 
- You'll find your CSE15L username in the following page under "additional accounts". 
(All CSE15L accounts start with "cs15lwi23") 
- Click on the account, in the resulting page, there will be a prompt allowing you to set a password. 
- After resetting your password, your account is ready to go!  (You may have to wait a few minutes for your new password to properly process)

## Logging into CSE Basement 
- Once you enter the terminal, enter the command `ssh yourusername@ieng6.ucsd.edu` <br>
![image](https://user-images.githubusercontent.com/122556045/212213553-12150c28-b898-41a2-a411-99c4001fdc35.png)
- Following this you'll get a message like the one below, simply put, answer yes. 
![image](https://user-images.githubusercontent.com/122556045/212213887-2d20a329-7c87-4365-8be3-8a0679391dd6.png) 
- After answering yes, you'll be prompted to enter your account password, if you already 
  previously updated your password in the steps above, simply enter what password you currently have 
  on your account. **Note: When you type your password, for security reasons, you won't see the characters, so type carefully or copy paste!**
- If everything was done correctly, you should get a screen like this 
![image](https://user-images.githubusercontent.com/122556045/212214566-2c864f17-34fd-40c1-bc45-1ba4b9e5ecbc.png) <br>
**From here we can start entering commands**. 

# Terminal command excersizes 
You can input a variety of commands into the terminal, you'll learn more throughout the course of this class 
and your career, for now here are some basic commands:  

- `cat (path1)(path2)` **Prints out the contents of one or more files given by the paths** 
- `ls (path)` **"List" Used to list the files and folders of a given path** 
- `pwd` **"Print working directory" Used to display the current working directory** 
- `cd (path)` **"Change directory" Used to switch the current working directory to the given path**

Since we are in the a public CSE Basement server, one thing that's useful to try is getting access to the text of a 
public file. In this case we can access it by using the cat commmand on the path /home/linux/ieng6/cs15lwi23/public/hello.txt 
you should get the following result:  

![image](https://user-images.githubusercontent.com/122556045/212217484-c9718351-dd53-4bc3-8516-ba80adbdd79f.png) <br>
(this is the content of the public text file)

# Closing remarks 
Now that you have your account set up, are able to log in, and use basic commands, you are ready for CSE15L! 















