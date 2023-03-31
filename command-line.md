# What is the Command Line
The window, which is usually called the command line or command-line interface, is a text-based application for viewing, handling, and manipulating files on your computer. It's much like Windows Explorer or Finder on the Mac, but without the graphical interface. Other names for the command line are: cmd, CLI, prompt, console or terminal. It is one of two ways to interact with your computer. Here we are going to do a simple primer of all the commands needed to start a project.
Shortcut To Open the Terminal On Mac
To open your terminal on the mac press the  ⌘ and space button together. Then type in Terminal.
Begin by listing ls the contents of the terminal. Type the command below:
```console
$ ls
```
That should list all the folders on your machine from there. Now make your project directory by typing ```mkdir projects``` and let's change directories by typing ```cd projects``` so we can get inside the project folder. we can do the commands together by typing ```&&```.
```console
$ mkdir projects && cd projects
```
Now that the project folder is made, time to create a file. We are going to use the same command as above to make a ```profile-site``` folder and change directory into the ```profile-site``` folder then use the ```touch``` command to create an index file in the ```profile-site```
```console
$ mkdir profile-site && cd profile-site
$ touch index.html
```
That's it. you have your first file!
## Lets Make The Project Structure!
Now we are gonna flesh out the project structure. Let's make two folders, one called ```styles``` and the other called ```scripts``` and add files called ```styles.css``` and ```scripts.js```
```console
$ mkdir styles scripts
$ touch styles/styles.css scripts.scripts.js
```
Oh no! We messed up the name of the scripts file! Looks like we have to delete it. We can do that for folders and files by using ```rm -rf```. Lets fix our mistake.
```console
$ rm -rf scripts.scripts.js
$ touch scripts/scripts.js
```
Great job on your first project code structure!

## Additional Resources

This section contains helpful links to related content. It isn’t required, so consider it supplemental.

[The Art of Command Line](https://github.com/jlevy/the-art-of-command-line#readme) is a complete beginner’s pro-maker. It serves as an open-source repository. This also has a lot of pro tips!

The online book, [Learn Enough Command Line to Be Dangerous](https://www.learnenough.com/command-line-tutorial) is a great resource for mastering the command line. Chapter 1 is free and provides a good introduction to command line tools. The rest of the book is not free and goes into more depth than you really need at this point, but feel free to buy and read the rest of the book if you like.

[ExplainShell.com](http://explainshell.com/) is a great resource if you want to deconstruct a particularly strange shell command or learn how Bash works through guess-and-check.

[Unix/Linux Command Cheat Sheet](https://files.fosswire.com/2007/08/fwunixref.pdf) contains a list of important commands that you can refer to regularly as you become familiar with using Linux. You can print it out so you can have a physical copy with you when you’re not at your computer.

[Command Line Flashcards](https://flashcards.github.io/command_line/introduction.html) by flashcards.github.io.

[Video Series from LearnLinuxTv](https://www.youtube.com/playlist?list=PLT98CRl2KxKHaKA9-4_I38sLzK134p4GJ) contains 24 videos explaining the basics of the command line. Videos are brief enough for beginners but, at the same time, detailed enough to get you started and light your inner curiosity.

