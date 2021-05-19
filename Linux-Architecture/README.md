# Linux Architecture 
It consists of Kernel and Shell. They have been discussed in detail further. 

## Kernel 

The kernel is a *computer program that is the core of a computers operating system*, with complete control over everything in the system. It *virtualizes the common hardware resources* of the computer to provide each process with its virtual resources. This makes the process seem as it is the sole process running on the machine. The kernel is also responsible for *preventing and mitigating conflicts between different processes*. It manages the following resources of the Linux System:
- File Management 
- Process Management 
- I/O Management 
- Memory Management 
- Device Management 

## Shell 
A shell is a special *user program* which provides an *interface to the user to use operating system services*. Shell accepts human-readable commands from user and converts them into something which kernel can understand. It is a *command language interpreter* that execute commands read from input devices such as keyboards or from files. The *shell gets started when the user logs in or start the terminal*.

![linuxshell](https://user-images.githubusercontent.com/44089458/113505489-d8b1e880-955c-11eb-9447-c63ac9671211.jpg)


Shell is broadly classified into two catergories: 
1. Command-Line Shell 

Shell can be accessed by the user using a command-line interface. A special program called Terminal in Linux/macOS or Command Prompt in Windows OS is provided to type in the human-readable commands such as “cat”, “ls” etc. and then it is being executed. The result is then displayed on the terminal to the user. A terminal in Ubuntu 20.04 system looks like this –
![linux5](https://user-images.githubusercontent.com/44089458/113505470-b28c4880-955c-11eb-9813-9a59ca47c578.jpg)


2. Graphical Shell 

Graphical shells provide means for manipulating programs based on graphical user interface (GUI), by allowing for operations such as opening, closing, moving and resizing windows, as well as switching focus between windows. Window OS or Ubuntu OS can be considered as good example which provide GUI to user for interacting with program. User do not need to type in command for every actions.


## Types of Shell

- BASH (Bourne Again SHell): It is most widely used shell in Linux systems. It is used as default login shell in Linux systems and in macOS. It can also be installed on Windows OS.
- CSH (C SHell) - The C shell's syntax and usage are very similar to the C programming language.
- KSH (Korn SHell) - The Korn Shell also was the base for the POSIX Shell standard specifications etc.

## Shell Relationship 

When you move from one shell to another, UNIX remembers the path you followed by creating a parent-child relationship. Your *login shell is always the most senior shell in the relationship* - the parent or grandparent depending on how many shells you have used.

## Command Prompt or Prompt 
It is a short text message at the start of the command line on a command-line interface. Prompts are found on the command line interface of any operating system that provides a command-line interface. It is a default prompt on the bash shell which is a default shell on Linux containing the name of the user, the name of the computer and the name of the current directory(i.e., the directory in which the user is currently working).

## Linux Architecture

![linux6](https://user-images.githubusercontent.com/44089458/113505501-e7989b00-955c-11eb-8d4f-6bb2e2292086.jpg)

