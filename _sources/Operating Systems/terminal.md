# Terminal Basics

## The Terminal
We will be living in the terminal when using linux.

The terminal can be accessed in the top left of your screen (circled in red):
![Alt text](terminal.png)

The most commands we will use to start at:

| Command | Use | Notes |
|---------|-----|-------|
|pwd|see the file you are at|*present working directroy*|
|cd |change file |*change directory*|
|ls|listing files and folder in the foler you are at|*listings*|
|mkdir|make a new directory|*make directory*|
|rmdir|delete an existing directory|*remove directroy*|
|echo|display text||
|cp|copy a file or directory|*copy*|
|rm|remove a file or directory|*remove*|
|mv|move a file or directory|*move*|
|locate|locate a file or directory|*locate*|
|updatedb|update the database that keeps track of files and directories|*update database*|
|passwd|change your password|*password*|
|man|see the documentaiton foor a given command|*manuscript*|

## Navigating the File system

### Excercise 1

The goal of this excercise it familirize yourself with common terminal commands. You will learn to use <code>cd</code>, <code>pwd</code>, <code>ls</code>, and <code>sudo</code>. You will also get familiar with the basic file structure of your system.

Open your terminal and do the following:
1. type <code>pwd</code> and hit *enter*

    This will show you where we are at the computer.
2. type <code>cd ..</code> and hit *enter*

    This will go backwards in the file system.
3. type <code>pwd</code> and hit *enter*

    This will let you see where you are now.

4. repeat steps 2 and 3, until you see a <code>/<code>:

    The forward slash is is your base folder. 
5. type <code>ls</code> and hit *enter*:
    
    This allows you to see what folders and files you can access from the current folder

6. type <code>cd root</code> and hit *enter*
    
    You may see an error "cd: permission denied: root". This is because you are not the administrator. In this case do the following:
    1. type <code>sudo -s</code> and hit *enter*: this will prompt you for the administrator password. If you haven't changed it, it should still be *kali*.
    2. type in the password. you wont see the password, but it is being typed. Hit *enter* when you are done.
6. type <code>pwd</code> and hit *enter*.
7. If you are not in the <code>/</code> directory, navigate to it.
8. type <code>cd root</code> and hit *enter*


At this point your terminal should look something like this:
    ![Alt text](ex1a.png)

 *note: from now own, enter after you are instructed to type something.*

9. Now that your are in the root type <code>clear<code> to clear the terminal.
10. Type <code>ls</code> to see what files are available: you will see nothing is availble.
11. Navigate to the home folder by typing <code>cd /home/<code>.
12. Navigate to the Kali folder by typing <code>cd kali<code>.
13. Type <code>ls</code>
14. Navigate to the Desktop folder (note this is case sensitive - type *Desktop* not *desktop*).
15. Now type <code>ls /</code>

    This will allow you will to see all the files in the base folder.

16. Type <code>pwd</code>
17. Type <code>ls</code>
    
    This may be empty as your desktop folders may be empty.

18. At this point we are in the Desktop folder, but what if we wanted to access a folder that is not nexted underneath the Dekstop? 

    Say you wanted to access <code>/etc/</code> type: <code>cd /etc/</code>

19. Now say we want to go back to Desktop? Type:  <code>cd /home/kali/Desktop</code>

20. We can also see what exists in another folder with out accessing:

    Type <code>ls /home/</code> to see what is in the home directory.

21. Now make sure you are in the Desktop. What if we wanted to create a new folder? Type <code>mkdir name</code>. Type <code>ls</code> to see it was created. 

22. Lets delete the new folder. Type <code>rmdir name</code>.


### Excercise 2
The goal of this excercise it familirize yourself with some more common terminal commands. You will learn to use <code>echo</code>, <code>cp</code>, <code>rm</code>, <code>mv</code>, and <code>locate</code>. You will also get familiar with the use of arrows to navigate to previous commands.


1. Navigate back to the base folder.
2. Navigate to the root. Try to see what files exist. Now type <code>ls -la</code>. You'll see a lot more files that didnt exist before. These are hidden files.

    ![Alt text](hidden.png)

3. Navigate to your Desktop.
4. Type <code>echo "hello world"</code>

    This is like a Python print statement

5. Hit the up arrow on your keyboard. The previous comman should show up. Complete it look like: <code>echo "hello world" > hello.txt</code> and hit enter.

    This will print the words to a new document called *hello.txt*. Feel free to go to your desktop, and find the new document. Or type <code>ls</code> to see it got created.

6. What if we want to move copy the file to a nother location? Type <code>cp hello.txt /home/kali</code>. Navigate to <code>kali</code> and see how it moved a folder.

    ![Alt text](copy.png)

7. What if we want to delete the file? <code>rm hello.txt</code>. Notice it only deletes it in the directory you are working on.

At this point my terminal looks like these:
    ![Alt text](remove.png)

Notice that <code>hello.txt</code> exists in the <code>kali</code> directory but not the <code>Desktop</code> directoy. 

8. Move the text file to a different directoy <code>mv hello.txt Downloads/</code>

    ![Alt text](move.png)

9. Navigate back to the base folder. Now what if we wanted to find our text file? Type <code>locate</code>.

    If you get a message of the form <code>plocate: no pattern to search specified</code>, you should be good to go to the next step. If you get a message of the form <code>locate command not found</code> Run:
    <code>sudo apt update</code>
    <code>sudo apt install mlocate</code>

10. Once in the base folder type <code>locate hello.txt</code> to find the directoryt in which this file exists. 
    
    If you get a message of the form <code> No such file or directroy</code>, run <code>sudo updatedb</code> so kali can locate it in the future.

### Excericse 3

The goal of this excercise it familirize yourself with a few more common terminal commands. You will learn to set your password, and use the <code>man</code> command.

1. Right now we are using the default password, thats not very secure. You can update your password as following:

    ![Alt text](passwd.png)
     
    *Remember, passwords wont show up as being typed, but the terminal will read them.*

2. One more useful thing for using the command line, is to use the <code>man</code> command to learn some more about a commnad you are using. Try typing <code>man ls</code> to see how this command works.
