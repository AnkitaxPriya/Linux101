# Linux Commands 

## Basic Linux Commands 
1. ls

Used to list the contents in a folder like this:

```
$ ls
```

![linux1](https://user-images.githubusercontent.com/44089458/113504949-5c69d600-9559-11eb-8ccb-ed41c88a731c.jpg)


2. man

You can learn about options and arguments to be used in any command in Linux. man(man is short for manual) is used to give a description of any Linux command like this:

```$ man ls
```

Note: To quit from the 'man' or the manual page type 'q'.

![linux 3](https://user-images.githubusercontent.com/44089458/113504955-68559800-9559-11eb-9c85-3931c10cfc00.jpg)

3. file
This command can be used to find the details of a file name.

```
$ file file_name.ext
```

![linux2](https://user-images.githubusercontent.com/44089458/113504964-75728700-9559-11eb-89a3-8d47ebd14398.jpg)

4. stat
This command is used to display ownership and modification information etc.

```
$ stat file_name.ext
```

![linux4](https://user-images.githubusercontent.com/44089458/113504971-802d1c00-9559-11eb-82ee-1827487cb4fc.jpg)

5. pwd 
The 'pwd' stands for 'Print Working Directory'. It prints the path of the working directory, starting from the root. It is shell a built-in command(pwd) or an actual binary(/bin/pwd). Here is the syntax:

```
$ pwd
```

![linux 6](https://user-images.githubusercontent.com/44089458/113505682-1105f680-955e-11eb-8926-14112a98ce69.jpg)

6. cd 
The 'cd' command in Linux known as 'Change Directory' command is used to change the current working directory to a new directory name that you have specified after 'cd' command. Here is the syntax:

```
$ cd [directory]
```

![linux 7](https://user-images.githubusercontent.com/44089458/113505714-50ccde00-955e-11eb-9e73-910ea59f4013.jpg)

7. clear 
The 'clear' is a standard Unix computer operating system command that is used to clear the terminal screen. This command will ignore any command-line parameters that may be present. Also, the 'clear' command doesn’t take any argument and it is almost similar to 'cls' command on a number of other Operating Systems. Here is the syntax:

```
$ clear
```

Terminal before executing clear command: 
![notclear](https://user-images.githubusercontent.com/44089458/113505797-b8832900-955e-11eb-8fcd-334de847ab03.jpg)

Terminal after executing the clear command: 
![clear](https://user-images.githubusercontent.com/44089458/113505805-c89b0880-955e-11eb-8cf0-068e7b76ec99.jpg)


## Command Usage in Linux 

1. Case Sensitive:
Commands in Linux are case-sensitive. Hence upper case letter and lower case letters cannot be used interchangeably. The standard observations are:
- All standard Linux commands tend to be in lower case.
- All Linux commands are single-word commands.

Example: Here we have used 'ls' and 'LS' command to differentiate.

![cms](https://user-images.githubusercontent.com/44089458/113505897-39422500-955f-11eb-9633-726cac19cfeb.jpg)
Case sesitivity of Linux commands 

2. Locating Commands:
Every command of Linux is stored somewhere in the local machine and when a particular command is executed, it gets called from that particular location. The file of every command contains the program mainly written in C language. This location of the file can be known using the 'type' command in Linux. Here is the Syntax:

```
$ type Command_name
```

*Example: Locating the 'ls' command.

![ls](https://user-images.githubusercontent.com/44089458/113505954-845c3800-955f-11eb-8345-1ab7ad3bd3db.jpg)

3. The UNIX system is command-based i.e things happen because of the commands that you key in. All UNIX commands are seldom more than four characters long. They are grouped into two categories:

**Internal Commands**: Commands which are built into the shell. For all the shell built-in commands, execution of the same is fast in the sense that the shell doesn’t have to search the given path for them in the PATH variable, and also no process needs to be spawned for executing it.
Examples: source, cd, fg, etc.

**External Commands**: Commands which aren’t built into the shell. When an external command has to be executed, the shell looks for its path given in the PATH variable, and also a new process has to be spawned and the command gets executed. They are usually located in /bin or /usr/bin. For example, when you execute the “cat” command, which usually is at /usr/bin, the executable /usr/bin/cat gets executed.
Examples: ls, cat etc.

The type command in Linux can be used to identify whether a command is an Internal or an External command. Let's try to identify the 'cd' and 'ls'.
![cd](https://user-images.githubusercontent.com/44089458/113506052-149a7d00-9560-11eb-855c-f70a0a35c477.jpg)

Identifying the 'cd' and 'ls' command
- 'cd' shows "cd is a shell built in" which signifies that 'cd' is an internal command.

- 'ls' gives the location of the ls file signifying that it is an external command.

4. **Command Structure**
- Commands and arguments have to be separated by spaces or tabs to enable the system to interpret them as words.
- Any number of spaces can be used.

5. **Options in Command **
There are special types of arguments that are mostly used with '-' sign. For example using:

```
$ ls -l
```

Points to remember:
- '-l' is an argument to ls by definition. It a special argument known as an option. It is used to show long listing information about the file/directory.

- An option is normally preceded by a minus sign to differentiate it from filenames.

- There must not be any white space between '-' and 'l' but there must be whitespace between the command and the argument

- Options can be combined with only one ‘-’ sign
`ls -lat abc` is the same as `ls -l -a -t abc`

Example: Working of `ls -l` command.

![Screenshot 2021-04-04 161217](https://user-images.githubusercontent.com/44089458/113506131-9c808700-9560-11eb-83c2-261addaee747.jpg)

6. **Flexibility of Commands**

Combining Commands
- Linux allows you to specify more than one command in the command line.
- Each command has to be separated from the other by a ; (semicolon)

```
ls; pwd
```

- When a command line contains a semicolon, the shell understands that the command on each side of it needs to be processed separately The ; here is known as a metacharacter

*Example: The above command will first execute the 'ls' command listing the directory followed by the path of the working directory.*

![Screenshot 2021-04-04 161442](https://user-images.githubusercontent.com/44089458/113506191-f2edc580-9560-11eb-810a-dcf630a8ef5e.jpg)

7. **Flexibility of Commands**

Multiline Purpose 
- Though the terminal width is restricted to 80 characters, that doesn’t prevent you from entering a command, in one line even though the total width may exceed 80 characters.
- The command simply overflows to the next line
- Sometimes, it is desirable to split a long command line into multiple lines. In that case, the shell issues a secondary prompt, usually ‘>’ to indicate that the command line isn’t complete.

8. **The echo Command**

The echo command in Linux is used to display the line of text/string that is passed as an argument. This is a built-in command that is mostly used in shell scripts and batch files to output status text to the screen or a file. Here is the syntax.

1. To display in multiple lines:

```
$echo “Line 1

>Line 2

>Line 3”
```

2. To display in single lines:

```
$echo “Line 1”
```

![Screenshot 2021-04-04 161855](https://user-images.githubusercontent.com/44089458/113506299-86bf9180-9561-11eb-9f27-16ec9cebe823.jpg)
