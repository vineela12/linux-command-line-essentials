           
          
           
 BASIC INTRODUCTION TO SHELL 
===========================================================

  

		1. Let's Get Started With Basic Introduction.
		2. Basic Shell Commands.
		3. File Compression.
		4. Permissions.
		5. Filters.
		6. Job Control.
		


**1. Let's Get Started With Basic Introduction.**
---------------------------------------


UNIX is a computer Operating System which is capable of handling activities from multiple users at the same time.Users direct the operation of the computer by entering commands as text for a command line interpreter to execute or by creating text scripts of one or more such commands.The shell provides you with an  user interface to the UNIX system. It gathers input from you and executes programs based on that input. When a program finishes executing, it displays that program's output. 

The most influential Unix shells have been the Bourne shell and the C shell.
>######Bourne shell :- ######
>The default prompt is $ character for the Bourne-type shell.Various subcategories for Bourne Shell are Bourne shell(sh),Korn shell(ksh),
Bourne Again shell(bash),POSIX shell(sh)

>######C shell :- ######
>The C shell. If you are using a C-type shell, the default prompt is the % character.
>The default prompt is % character for the C shell.Various subcategories for 
C shell are C shell ( csh),TENEX/TOPS C shell ( tcsh)

The Bourne shell was the first shell to appear on UNIX systems, thus it is referred to as "the shell".

----------
**What's a Terminal :**

It is a program called a terminal emulator.This is a program that opens a window and lets you interact with the shell.Most linux distributions supply several such as: Gnome-terminal,Konsole, XTerm, rxvt, kvt, NXTerm and EXTerm.

----------
**Directory Structure in LINUX systems.**

![Alt text](http://fsl.fmrib.ox.ac.uk/fslcourse/unix_intro/tree.gif)

Files in Linux system are arranged in Hierarchical Directory Structure.Which means that they are organized in a tree-like pattern of directories.The root directory contains files and sub-directories,which contain more files and sub-directories and so on. 

------------------------

**2 .Basic Shell Commands.**
----------------------------------


>**NOTE :**The shell is case sensitive.

**1. The ls** :-

The ls command is used to list the contents of a directory.

1. **ls** --- Lists your files.
2. **ls -l** --- List your files in long format.
3. **ls -a** --- Lists all the files.
4. **ls /bin** --- List the files in the /bin directory.
5. **ls -la** --- List all files in the parent of the working directory in long format.

**2. Use an Editor to write a new file :-**

Follow the below commands to open the file in the editor.

1. **emacs filename** --- Emacs editor that lets you create and edit a file.
2. **vi filename** --- vim editor that lets you create and edit a file.



**3. Want to see the part of the file?**

Use this command:

1. **more filename** --- Shows the first part of the file.hit q to quit and 
"/pattern" to search for a pattern.



**4. File Operations:-**


**Copy Command:** Copy files and directories.


1. **cp file1 file2** --- Copies the contents of file1 into file2.
2. **cp -i file1 file2** --- (-i) interactive option is specified if file2 exists,the user is prompted before it is overwritten with the contents of file1.
3. **cp file1 dir1** --- Copy the contents of file1 inside of directory dir1.
4. **cp -R dir1 dir2** --- Copy the contents of the directory dir1.If directory dir2 doesnot exist,it is created otherwise,it creates a directory named dir1 within directory2.
5. **cp * .txt**   text files --- Copy all files in the current working directory with names ending with the characters ".txt" to an existing directory named text-files.

**Move Command:** (mv) command moves or renames files and directories on how it is used.It will either move one or more files to a different directory,or it will rename a file or directory.

1. **mv file1 file2** --- Moves the file from file1 location to file2 location.
2. **mv -i file1 file2** --- (-i) interactive option is specified if file2 exists,the user is prompted before it is overwritten with the contents of file1.
3. **mv file1 file2 file3 dir1** --- The file1,2,3 are moved to directory dir1.If dir1 doesnot exist,mv will exit with an error.
4. **mv dir1 dir2** --- Moves all the files from dir1 to dir2.


**Remove Command:** The rm command removes(deletes) files and directories.

1. **rm file:** Removes a file.
2. **rm file1 file2** --- Removes file1 and file2.
3. **rm -i file1 file2** --- Each file is deleted.
4. **rm -r dir1 dir2** --- Directories dir1 and dir2 are deleted along with all of their contents.
5. **rm * ~** --- Delete all files in the current working directory that end with the character "~".Some applications create backup files using this naming schema.Using this command will clean them out of a directory.

**Hey!! Want to Make a Directory??OR wanna know more about them? Go This way!**

1. **mkdir dirname:** --- Creates Directory or make a new directory.
2. **cd dirname:** --- Change Directory.
3. **pwd:** --- tells you where you currently are.(present working Directory).
4. **file:** --- If you see interesting file,use the file command to determine the contents.

**These might help you when you are messed up.**

1. **type** --- Display information about command type.
2. **which** --- Locate a command.
3. **help** --- Display reference page for shell builtin.
4. **man** --- Display an on-line command reference.
   *Example:  man ls*
5. **ff** --- find the files anywhere on the system.
6. **grep string filename(s)** --- look for the string in the files.
7. **w** --- tells you who's logged in,and what they're doing.
8. **who** --- tells you who's logged on,and where they're trying to come from.
9. **whoami**--- Your username is returned.
10. **finger** --- Pointing your ownself.
11. **last -l username** --- tells you when the user last logged on or off and from where.
12. **passwd** --- let's you change your password.
13. **last yourusername** --- lists your last logins.
14. **diff file1 file2** --- compares files and shows where they differ.
15. **tr** --- Translates characters 
*Example: Dos text file -->Unix style test file*
16. **lynx** --- lets you browse the web from an ordinary terminal.
 
**Been tried doing all these? STOP!! Try this out and have some fun**

1. **webster word** --- looks up the word in an electronic version of webster's dictionary and returns a definition.
2.  **date** --- shows the current date and time.
3.  **cal** --- shows a calender of the current month.
4.  **wc filename** --- tells you how many lines,words and characters are there in a file.

-----------
**3. File Compression**
---------------------

1. **gzip filename** --- compressess files,so that they take up much less space.
2. **gunzip filename** --- uncompresses files compressed by gzip.
3. **gzcat filename** --- lets us to look at a gizipped file without actually having to gunzip it.

----------

**4. Permissions**
-----------------------
hmm...Premissions are always important aren't they? You can only understand their importance if you were in a hostel. Just kidding ;-)

Will we use these commands often when we deal with premissions.

1. **su or sudo** --- Temporarily become the superuser.
2. **chown** --- change file ownership.
3. **chgrp** --- change the file's group ownership.
4. **chmod options filename** --- Let's you change the read,write and execute permissions on your files.


![Alt text](http://www.samba.org/samba/docs/man/Samba-HOWTO-Collection/images/access1.png)

------------------
**5. Filters**
--------------------------------------

1. **sort** ---sorts the input and outputs the sorted result.
2. **grep** ---it examines each line of data it receives from standard input and outputs every line that contains a specified pattern of characters.
3. **head** --- outputs the few lines of its input useful for getting the header of a file.
4. **tail** --- outputs the last few lines of its input.

----------


**6. Job Control**
------------------------------
There are several commands that can be used to control processes.

1. **ps -u yourusername** or alias (jobs) --- Lists your processes in your system that are running.
2. **Kill ID or Kill all** --- Kills the processes with the particular id or all id if we use all.
3. **bg/fg** --- put a process in the background/foreground.



 
