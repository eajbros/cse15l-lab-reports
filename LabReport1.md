# Lab Report 1

## `cd` Command
---
---
## `ls` Command
---
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
