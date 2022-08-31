---
layout: post
title:  "Using the command (or prompt) line for beginners"
date:   2022-08-03
categories: Programming Learning
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

<p><img src="/assets/images/command-line_115191.png" alt="Command line symbol" width="200"></p>

*This is part of the content I learned during my first week of the Makers Academy Pre-course, and as such, writing this posts are a way of reviewing what I have learnt and hopefully helping other people which are also trying to get into the tech industry.*

Ever saw a movie where someone that looked quite nerdy was getting a computer to do what they wanted by writing weird commands on the screen?

The **command line (or prompt)** is a way to communicate directly with your computer without having to go through the GUI (Graphical User Interface, or all the pretty windows and icons we normally see and click on while using out PC). It is a **very fast and efficient way of working with your computer** and the only way on some of them, and you definitely want to know how to make the best of it if you are considering a career in tech.


## How to open the command line or command prompt

<p><img src="/assets/images/hannah-joshua-46T6nVjRc2w-unsplash (1).jpg" alt="Command key by Hannah Joshua" width="200"></p>

- To access this feature on **Windows**, you can press the **Windows key + X**
- For **Mac users**, you can press **Command + Space** and **type in “Terminal”**, or pressing F4, locate the “Other” folder and click on “Terminal”.
- For **Linux users**, it is as simple as pressing **Ctrl + Alt + T**

Once you have followed the instructions, a small window like this one will pop-up:

<p><img src="/assets/images/commandline1.png" alt="Command line" width="600"></p>

And that is your command line! Now you are ready to start giving orders to your computer. It can appear quite complicated at the beginning, but if you keep practising, you will very quickly become proficient at it.

On the example image, you can see the name of the user that is logged in (pattyflowers), the name of the computer after the @ symbol (pattyflowers-HP-ProBook-455-G2), and the current directory (‘~’ is what Linux uses to indicate the home directory). Then, you will have wither a ‘%’ on zsh (Mac) or “$” on Bash (Linux), and this will mean the end of the prompt.

Once you start writing a lot of commands, you will be able to navigate through them with the up and down arrows on your keyboard.

To **write a command**, just type it in the command line and **press Enter to execute it**, easy! 
If you need to **stop a process from running**, you can normally do so with **Ctrl + C** (Linux) or **Command + '.'** (Mac).
You can write several commands one after the other using '&&' between them.

If you need to copy or paste any text within the command line, sometimes you will not be able to do it with the usual `Ctrl + C` and `Ctrl + V`. This sounds very basic but it gave me some headaches when I started using the command line:

- On Windows 10, you can enable this option. [Here is a tutorial on how to do it.](https://www.laptopmag.com/articles/how-to-windows-10-command-prompt-copy)
- On Linux, you can use `Ctrl + Insert` or `Ctrl + shift+C/V` for copying/pasting text. You can also just right click on your mouse and select the action.
- On Mac, you can simply press `Command + C/V`

Note: If the text you are pasting includes the return character at the end of the line, the command will be executed straight away without you pressing `Enter`, so bear this in mind!


<p><img src="/assets/images/tai-bui-393l7SYoM7w-unsplash.jpg" alt="Cat on computer by Tai Bui" width="300"></p>


## Directory operations

First of all, you will have to **learn how to navigate through the folders** in your computer and make sure you are in the right one while you are working. You will find that many commands cannot be run directly on a particular folder as it doesn’t have the file you are trying to work with, so try not to get frustrated, you will get used to this!

Here is a table with some **basic commands** you will need to know in order to move around your computer and explore:

| Command | Meaning | Description  | Examples |
|---------|----------|-----------------|-------|
|`whoami` | Who am I?| Shows the current user's username | Example of output: `pattyflowers`
| `date` | date | Shows the system date | Outputs: `Thu 18 Aug 13:00:02 BST 2022` |
| `pwd` | print working directory | Shows (prints) the current directory you are in. | Outputs: `/home/catfromspace` |
| `ls` | list | Lists all the files and directories within your current directory. | Outputs: `Desktop` `Documents` `Downloads` `Pictures` |
| `cd *dir*` | change directory | Goes to the directory of your choice (*dir*) | `cd Desktop` would take us to `home/catfromspace/Desktop`|
|`cd ..` |change directory (up) | Goes up one directory | If we are on `/home/catfromspace/Desktop`, it would take us to `home/catfromspace`
| `man *command*` | manual | It displays a full manual on how to use the chosen command | `man ls` would display <img src="/assets/images/commandlinemanual.png" alt="Command line manual example" width="400">|
|`mkdir *dir*` | make directory | Makes a new empty directory (folder) with the chosen name | `mkdir MyNewFolder` |
| `rmdir *dir*` | remove directory | Removes a directory (folder) as long as it is empty | `rmdir MyNewFolder` |

*Note: The words within asterisks are the ones you need to fill in with the directory, folder, command or file of your choice.*

Here is an example of the commands we have learnt so far and what they do:

<p><img src="/assets/images/commandline2.png" alt="Command line examples" width="600"></p>

## Working with files

Now that you are able to check and navigate around your folders, it is time to learn how to woek with the files you have on your computer.

| Command | Meaning | Description  | Examples |
|---------|----------|-----------------|-------|
| `grep *pattern* *files*` | Global Regular Expression Print | Searches for a *pattern* within the chosen *files*. You can use it with Regular Expressions. | `grep 'some text' MyFile` | 
| `find *dir* -name *name*` | Find | Searches, starting on the chosen directory, for files with the desired name | `find . -name "MyFile"` '.' stands for the current directory we are in, but you can write the path to any directory you wish. There is a lot more `find` can do for you, you can read more about this using `man find` |
| `wc *file*` | Word count | Returns 3 numbers: the lines, words and characters within the file | `wc blog.odt` returns `116   625 33329 blog.odt`|
|`touch *file*` | create, change and modify timestamps of a file | Normally used to create new files| `touch 'MynewFile.txt'`|
|`cat *file1* *file2* > CombinedFile` | Concatenate | Combines the content of 2 or more files into a new file | `cat 'TextFile' 'OtherTextFile' > 'CombinedTextFile'`
| `cat *Textfile*`| Concatenate | When used with only one text file, it allows you to display the text directly on the command line| |
| `cat > *TextFile*`| Concatenate| It allows you to create short text documents directly in the terminal, prompting you for text| |
|`echo "someText" > text.txt` | | It is a command that outputs the strings that are passed to it as arguments. We can use it to create short text files or to print on the screen what we write|To create a short text file with the text we write: `echo "Hello, world" > hello.txt`, to print some text on the terminal: `echo "This text will print on the terminal!`
| `less *TextFile*` | Less | It displays the contents of a text file or a command output one page at a time. Press [here](https://linuxize.com/post/less-command-in-linux/) for a tutorial on how to navigate through the text| |
|`head -number *file*` | Head | It will output the specified number of lines from the beginning of the file. If the number is empty, it will output 10 lines of text | `head -3 MyFile` or `head MyFile`|
|`tail *file*`| Tail | It will output the last 10 lines of text | `tail MyFile`|
|`file *file*`| File | Outputs the type of the file | `file blog.odt` outputs `blog.odt: OpenDocument Text`|
|`cp *file1* *NewFile*` | Copy | Copies *file1* into a new file called *NewFile*. If you specify a path, you can create a copy in a different directory.| `cp MyFile MyFileCopy` or `cp MyFile home/catfromspace/MyFileCopy`|
|`rm *file*`| Remove | Will eliminate the chosen file from the computer.  | `rm 'MyFile.txt`|
|`mv *file1 path* *file2 path*` | Move | Moves the chosen file from one location to the other. Can also be used to rename files if you choose the same path for both.| `mv home/catfromspace/sardines.pdf home/foodsilike/sardines.pdf`|


## Switches or Flags

Switches or flags are a combination of a hyphon and a letter that we can use to change the functionality of the commands. You can use several flags on a single command, and instead of writing `ls -l -A` you can also combine them: `ls -lA`

Here are some examples using the commands we already know: 

| Command with flag | Description  |
|---------|-----------------|
|`rm -i`| (interactive) Will prompt for confirmation that you want to delete each file, useful to delete some files but not others.|
|`rm -f`|  Will remove every file even if protected, **do not try it at home!**|
|`grep -i` |Case insensitive search|
|`ls -lA`| You can use it to display all directories including hidden ones. |

## Wildcards
When using the command line and handling lots of different files, it is very useful to be able to select only the files we want to see, and that is why we will use an asterisc ('*') as a wildcard. 

For example, if we write the following command `ls *.pdf` we are asking the computer to list only the pdf files.

`grep *YHQ NumberPlates` will look for a some text that ends in YHQ in the file NumberPlates, whilst `grep 849* Numberplates` will search for some text that begins with 849.

`find . -name "*.pdf" -print` This command will allow you to find files, starting with the current directory, which name ends in '.pdf' and will print them to the command line.

<p><img src="/assets/images/tra-my-BjL7XCugMNY-unsplash.jpg" alt="Cat on keyboard" width="400"></p>

And that is all for today, I hope it wasn't too intense! Inn our next post, we will discover some more advanced commands and concepts regarding the command line, see you then!
