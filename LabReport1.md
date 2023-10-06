# Lab Report 1
---
## `cd` Command
## _Command with no arguments:_
```
[user@sahara ~]$ cd
[user@sahara ~]$
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > Since no argument was passed into the `ls` command, the current directory did not change at all and nothing happened.

- Was this an error?
  > This was not an error.

## _Command with a path to a directory:_
```
[user@sahara ~]$ cd /home/lecture1/messages
[user@sahara ~/lecture1/messages]$
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > The path to the directory changed the current directory to that path, making the new working directory `/home/lecture1/messages`.

- Was this an error?
  > This was not an error.

## _Command with a path to a file:_
```
[user@sahara ~]$ cd /home/lecture1/messages/fr.txt
bash: cd: /home/lecture1/messages/fr.txt: Not a directory
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > Since `/home/lecture1/messages/fr.txt` is the path to a file and not a directory, we cannot change the working directory to that path.
  
- Was this an error?
  > This was an error because we tried to pass a path to a file in a command that needs a path to a directory.
---
## `ls` Command
## _Command with no arguments:_
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
- What was the working directory when the command was run?
  > `/home/lecture1` was the working directory.

- Why this output?
  > With no arguments, the `ls` command was run on the working directory by default. Therefore, the command printed out a list of all of the files and folders inside the path `/home/lecture1`.

- Was this an error?
  > This was not an error.



## _Command with a path to a directory:_
```
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  fr.txt  zh-cn.txt
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > With a path to a directory as the argument to the `ls` command, the command listed all of the files and folders inside the given directory. This consisted of the four .txt files inside the folder.

- Was this an error?
  > This was not an error.

## _Command with a path to a file:_
```
[user@sahara ~]$ ls lecture1/messages/fr.txt
lecture1/messages/fr.txt
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > With a path to a file as the argument to the `ls` command, the command only listed the file path itself. This is because there is no folders or files inside the file, so there is nothing else to list.
  
- Was this an error?
  > This was not an error.

---
## `cat` Command
## _Command with no arguments:_
```
[user@sahara ~]$ cat
hello
hello
world
world
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > The output was just a blank line until I typed something else into the terminal and it repeated it. I assume that passing no arguments waits for user input into the terminal because we did not give it any files to concatinate.

- Was this an error?
  > This was not an error, it seems like the command was intended to work this way.

## _Command with a path to a directory:_
```
[user@sahara ~]$ cat lecture1/messages
cat: lecture1/messages: Is a directory
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > Since the path was one to a directory, there was nothing for the command to concatinate, so it lets the user know that they have passed a path to a directory.

- Was this an error?
  > This was an error because the `cat` command could not be run on a directory.

## _Command with a path to a file:_
```
[user@sahara ~]$ cat lecture1/messages/fr.txt
Bonjour le monde!
```
- What was the working directory when the command was run?
  > `/home` was the working directory.

- Why this output?
  > The `cat` command printed out the contents of the file passed as an argument, this is because the command concatinates all files passed and prints out all of thier contents.
  
- Was this an error?
  > This was not an error.
---
