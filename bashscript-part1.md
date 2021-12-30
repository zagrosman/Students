# This is a tutorial to learn Bash scripting in Linux by H. Rasouli. 
******************************************************************
> December 27, 2021   ¯\_( ͡👁️ ͜ʖ ͡👁️)_/¯
******************************************************************
> You can follow me in Twitter to see more updates and notes about bioinformatics tools (https://twitter.com/H3nRasouli).
******************************************************************
> **“We cannot solve problems with the kind of thinking we employed when we came up with them.”** 
 *-Albert Einstein*
 ******************************************************************
 Let's go to learn new things there :)
 ![image](https://user-images.githubusercontent.com/17006122/147473546-2ed0caa7-3178-4dd6-86af-60c359ff0b73.png)

******************************************************************
# Useful online tutorials:

Here, I listed some websites that you can learn bash scripting from them. You should work with bash frequently to learn it in detail because all of your works in linux can be simply finalized using bash scripting:
1. https://ryanstutorials.net/bash-scripting-tutorial/bash-script.php
2. https://www.tutorialspoint.com/unix/shell_scripting.htm
3. https://www.youtube.com/watch?v=zWVV31NYi1U
4. https://www.javatpoint.com/bash

# Why bash script? (Part 1)
Bash is a command language interpreter. It is widely available on various operating systems and is a default command interpreter on most GNU/Linux systems. The name is an acronym for the ‘Bourne-Again SHell’.
 
# Learning bash

Note that the first command you type in your linux terminal is your firts bash code. In bash, everthing will written in linux terminal and you can simply see the results. The terminal is the heart of your linux OS so that you had to learn anything about it regarding the project you want to do. So, unlike Win OS you don't need to play with folders and paths and using bash scripting you are able to facilitate your computational analysis. There are many tutorials in the internet regarding bash scripting so that you are able to learn it in less than a month. The major benefit of bash scripting is that you can automate your linux-based jobs without spending more time to sophisticated processes. 
Bash scripts are used by Systems Administrators, Programmers, Network Engineers, Scientists and just about anyone else who uses a Linux/ Unix system regularly. No matter what you do or what your general level of computer proficiency is, you can generally find a way to use Bash scripting to make your life easier. Bash is a command line language. The name stands for Bourne Again SHell. It is an open source version of the Bourne Shell and was first released in 1989.
BASH is the default shell on most Linux distributions and Apple's macOS (formerly OS X). Recently, a version has also been made available for Windows 10.((https://gitforwindows.org/)). Scripting allows for an automatic commands execution that would otherwise be executed interactively one-by-one.

![image](https://user-images.githubusercontent.com/17006122/147474281-22e7e4e1-4321-49e8-b550-6ae279df8aa8.png)


Try it now! Use your keyboard and type some commands such as `date`, `cal`, `pwd` or `ls` followed by the ENTER key. The results are looking like the following images for your entered commands:

# `date`: this show the date on your terminal page

![image](https://user-images.githubusercontent.com/17006122/147476028-4501c83c-bbfd-465c-9c1b-6031ce9c8747.png)

# `cal`: this show a full calendar on your terminal

![image](https://user-images.githubusercontent.com/17006122/147476089-85c52f18-3e9b-4147-b8ed-ee67945472d6.png)

# `pwd`: this show the current path of your terminal directory:

![image](https://user-images.githubusercontent.com/17006122/147476208-0ba39ac1-b5ff-474c-afd9-7d25a4a79f55.png)

# `ls`: this show a list of all files that are existed in your current directory

Using this command you can see all content of a directory or folder without opening it. This helps you to manage your files and paths critically while you are working on linux terminal
![image](https://user-images.githubusercontent.com/17006122/147476282-6ec066c7-1d87-494a-b1aa-a1a345dfda4d.png)


# Create a new bash script file.
In linux this is a simple way to create a bash script file anywhere using a simple command. To do this, you will need only type `vi` and the name of your target file `test.sh` in the terminal. Then, a script will be created in your current directory. Before doing this, you should install `vi` using the following command:

`````
sudo apt-get install vim 
`````
# Vi or Vim command function
In linux, this command can create a new script file for you. After installation of `vim`, follow the below steps to create your first script
1. Open the terminal

![image](https://user-images.githubusercontent.com/17006122/147480789-b7176ca5-9475-45f3-9639-06b4d0294931.png)

2. Create a workfolder named `scripts` in `home` path

![image](https://user-images.githubusercontent.com/17006122/147480854-6e35f3ca-d283-40ec-b113-257d1d1b2d6a.png)

3. Using `cd` command navigate your terminal path to where the working folder is. 

````
cd scripts/
````

![image](https://user-images.githubusercontent.com/17006122/147480936-fab60599-80d2-4a67-8556-2bafc24e3d03.png)

4. Now, type `vi test.sh` in your terminal

````
vi test.sh
````

![image](https://user-images.githubusercontent.com/17006122/147481040-f56a7432-d367-4efe-9e85-bab972677bfc.png)


It will open a new script file for you in the linux terminal as shown in the following image:

![image](https://user-images.githubusercontent.com/17006122/147481100-246a1092-ba63-41cd-837e-587c1cc64895.png)


Now, press `insert key` on your keyboard. For your laptop, it seems the `0-key or ins` is the insert key of your keyboard. After pressing it, `insert mode` will be activated in the create script in the linux terminal. Then, the insert mode will be activated on the terminal and you can see it in the end of your script as shown:

![image](https://user-images.githubusercontent.com/17006122/147481318-312b9ee3-cc75-447d-b03b-9ecc59ec70f2.png)

Now, you can type `cal`, `date`, `pwd` and `ls` commands in this script to automate running of all commands you formerly run separately. 

![image](https://user-images.githubusercontent.com/17006122/147481646-5850096d-ac7d-4867-a2a5-fc574e3ba84d.png)


Next, press the `ESC` key on your keyboard to close the script. While you did it, you should type `:x` to save the script that created using `vi` command and then press the `enter` to go back the first line of terminal:

![image](https://user-images.githubusercontent.com/17006122/147481834-c80aa9b5-327d-4d4f-a7a7-dcc566b04a3d.png)

Note that after saving your script, a copy of its source will be saved in your working folder:

![image](https://user-images.githubusercontent.com/17006122/147481995-4c233746-3e2e-4947-ac27-1ed90071e932.png)


Now, you should activate your script using `chmod +x test.sh` command:

````
chmod +x test.sh
````

![image](https://user-images.githubusercontent.com/17006122/147482024-380678ef-5472-451b-beaf-cfde8c4cdbe8.png)

Now, your script is ready to run. To do this, just type `./test.sh` in your terminal 

````
./test.sh
````

After pressing `Enter key` all commands will be run on your terminal and you made the first automated script in your system. It will show the output of 4 commands for you without needing to enter all of them separately. This step helps you to save your time while working in linux and doing your jobs. Note that this is a simple automation process and in the next courses you will learn more about scripting in linux

![image](https://user-images.githubusercontent.com/17006122/147482320-f8a0a7f4-ceb2-4daf-9185-ccf4ab8a68e5.png)


As you can see, all outputs have shown after pressing the enter for your written script. 

This is why I love linux and doing my all taks there. I will keep you posted for more updates and courses in this term of learning. 


**Good Luck**




