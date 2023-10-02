# Lab Report 1 - Remote Access and FileSystem (Week 1)

Some of the commands we used today are `cd`, `ls`, and `cat`. We will explore the characteristics of each command by running each with *no* arguments, passing a path to a *directory*, and passing a path to a *file*. Each command will be run in the `lecture1` repository, with `home/` being the root directory.

## The `cd` command

1. Running the command with no arguments  
Running the command `cd` results in no change, as shown:
```
[user@sahara ~]$ cd
[user@sahara ~]$
```
This is because `cd` stands for change directory, and if no argument is passed, then the working directory will not change. It is not an error, it simply will not change anything.

2. Running the command with a directory  
Running the command `cd lecture1` will change the working directory to `lecture1`.
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
We can see the the working directory has changed on the second line. This is the expected output.

3. Running the command with a file
Running the command `cd lecture1/Hello.java` results in an error.
```
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory
```
This is an error because the command line explicitly tells us that the argument passed is not one that it accepts. `cd` only works with directories so passing a file will result in an error.

## The `ls` command

1. Running the command with no argument
Running `ls` will print the files within the current folder.
```
[user@sahara ~]$ ls
lecture1
```
Since the only folder within the working directory is `lecture1`, that is the only item that is printed.

2. Running the command with a directory
Running `ls lecture1` prints the contents of the `lecture1` folder.
```
[user@sahara ~]$ ls lecture1/
Hello.class  Hello.java  messages  README
```
The `ls` command prints the contents of a directory. Therefore, passing a path to a folder in the command will print the contents of the given folder. 

3. Running the command with a file
Running `ls lecture1/Hello.java` simply prints the given path.
```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```
`ls` prints the contents within a given path. Since the path is to file, and the only content within that path is the file, it will print the path.

## The `cat` command

1. Running the command with no arguments
Running `cat` results in the command line hanging, that is, the command is running but with no output and is not terminating
```
[user@sahara ~/lecture1]$ cat
^C
```
*Note, the `^C` is me forcefully terminating the command*. This could be considered an error, specifically a runtime error, because the command is not able to properly handle no arguments. `cat` should print the contents of a file, but since no file is passed, it does not know what to print.

2. Running the command with a directory
Running `cat lecture1` results in an error.
```
[user@sahara ~]$ cat lecture1/
cat: lecture1/: Is a directory
```
The `cat` command is unable to print the "contents" of a folder because the folder itself does not have any text. It may contain text documents, but the folder itself has no text, and therefore reuslts in an error.

3. Running the command with a file
Running `cat lecture1/messages/en-us.txt` prints the contents of the `en-us.txt` file.
```
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
```
As expected, the `cat` command prints the data within a file. This can also work for files that don't only contain text, like the `Hello.class` file which contains binary data. Here is the output: 
```
[user@sahara ~]$ cat lecture1/Hello.class
����@2

java/lang/Object<init>()java/lang/String




java/nio/file/Pathof;(Ljava/lang/String;[Ljava/lang/String;)Ljava/nio/file/Path;
!java/nio/charset/StandardCharsetsUTF_8Ljava/nio/charset/Charset;

java/nio/file/Files
readStringB(Ljava/nio/file/Path;Ljava/nio/charset/Charset;)Ljava/lang/String;
 java/lang/SystemoutLjava/io/PrintStream;
"#$
%&java/io/PrintStreamprintln(Ljava/lang/String;)V(HelloCodeLineNumberTablemain([Ljava/lang/String;)V
Exceptions/java/io/IOException
SourceFile
Hello.java!')*��*+,)9*2����L�  
```

---

This concludes a deep dive into the `cd`, `ls`, and `cat` commands.

