---
layout: post
title:  "Using the command (or prompt) line"
date:   2022-08-03
categories: Programming Learning
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---
*This is part of the content I learned during my first week of the Makers Academy Pre-course, and as such, writing this posts are a way of reviewing what I have learnt and hopefully helping other people which are also trying to get into the tech industry.*

Ever saw a movie where someone that looked quite nerdy was getting a computer to do what they wanted by writing weird commands on the screen?

The **command line (or prompt)** is a way to communicate directly with your computer without having to go through the GUI (Graphical User Interface, or all the pretty windows and icons we normally see and click on while using out PC). It is a **very fast and efficient way of working with your computer** and the only way on some of them, and you definitely want to know how to make the best of it if you are considering a career in tech.

# How to open the command line or command prompt
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

# Directory operations

First of all, you will have to **learn how to navigate through the folders** in your computer and make sure you are in the right one while you are working. You will find that many commands cannot be run directly on a particular folder as it doesn’t have the file you are trying to work with, so try not to get frustrated, you will get used to this!

Here is a table with some **basic commands** you will need to know in order to move around your computer and explore:

| Command | Meaning | Description | Output example |
|---------|----------|------------|-------|
| `pwd` | print working directory | Shows (prints) the current directory you are in. | `home\catfromspace` |
| `ls` | list | Lists all the files and directories within your current directory | `Desktop` `Documents` `Downloads` `Pictures` |
| `cd *dir*` | change directory | Goes to the directory of your choice (*dir*) | `cd Desktop` would take us to `home\catfromspace\Desktop`|
|`cd ..` |change directory (up) | Goes up one directory | If we are on `home\catfromspace\Desktop`, it would take us to `home\catfromspace`
| `man *command*` | manual | It displays a full manual on how to use the chosen command | `man cd`

The words within asterisks are the ones you need to fill in with the directory, folder or file of your choice.

Examples:

`$ pwd`   outputs ->  `home\catfromspace`

