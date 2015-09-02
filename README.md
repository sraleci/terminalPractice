# Laryea's Terminal Practice Assignment

## Assignment Details

You will create a website using only terminal to navigate and edit files. The website
will contain the following files and directories.

+ public/
	+ html/
		+ index.html
	+ stylesheets/
		+ style.css
	+ javascript/
		+ app.js

The html should contain an *h1* element that says "Hello World!", and a button that says
"toggle". The css should style the background to be *goldenrod* and the text to be *cornflowerblue*.
The javascript should make the button either show or hide the *h1* using the *click* event and
the *hidden* attribute.

## Hints

When you are navigating in the terminal, many commands that you use will reference
paths to files and directories (or folders).

+ The path ```/``` refers to the root directory. This the highest possible directory on your os, from which all other paths are based.
+ The path ```~``` refers to the home directory. This is usually your current directory when your terminal starts up.

When you are in the terminal, there is an idea of a current directory. Without
specifying an absolute path using ```/``` or ```~``` at the beginning of your path,
any paths you specify will be relative to your current directory. The current directory
can be changed using the ```cd``` command (meaning *Change Directory*).

+ The path ```.``` refers to the same directory relative to a specified directory (ie. the current directory).
+ The path ```..`` refers to the parent directory relative to a specified directory.

In other words:
1. **IF** your home directory (```~```) is located at ```/Users/bobsaget/```, and your current directory is ```~/Documents```
2. **THEN** the paths ```/Users/elvispresley```, ```./../../elvispresley```, and ```~/../elvispresley``` are all the same.
3. **THEN** the paths ```/Users/bobsaget/Documents/jsSnippets/numbers.js```, ```~/Documents/jsSnippets/numbers.js```, and ```jsSnippers/numbers.js``` are all the same.

## Useful Commands

### ls - List
Use this command to list files and directories within a specified directory. Using
the command by itself shows the files in the current directory, equivalent to using
```ls .```.

Usage

```
ls /Users/gwynnethpaltrow/Documents
```

This lists all of the visible documents and folders in the */Users/gwynethpaltrow/Documents*
directory.

### cd - Change Directory
Use this command to change your current directory.

Usage

```
cd /tmp
```

This changes your current directory to the *tmp* directory (designated for
temporary files) relative to the document root.

### mkdir - Make Directory
Use this command to create a directory.

Usage

```
mkdir ~/Documents/projectFolder/
```

This creates a directory named *projectFolder* in the *Documents* directory located in your home directory.

### rm - Remove
Use this command to remove files. The command can also be used to remove
folders, but requires you to specify additional options. To remove a folder,
use ```rm -rf```. The ```-rf``` is an option that stands for (**R**ecursive
**F**orce). This tells ```rm``` to remove a directory and everything inside
of it. 

**Note:** It is also important to remember that there is no Trash Bin when
you remove files. Using ```rm``` deletes files permanently.

Usage

``` 
rm ~/Documents/projectFolder/index.html
rm -rf ~/Documents/projectFolder
```

The first deletes the index file. The second command removes the projectFolder directory.

### vim - VI iMproved (Vi is the built in Unix text editor)
Use this command to edit files.

Usage

```
vim ~/Documents/projectFolder/index.html
```

This begins editing a file called *index.html* in the *~/Documents/projectFolder/* directory.

#### Vim Hints

+ Use ```i``` to enter *Insert* mode.
+ Use ```Esc``` to exit *Insert* mode.
+ While not in edit mode:
	+ Type ```:w``` to write (save).
	+ Type ```:q``` to quit.
	+ Type ```:wq``` to write and quit.
	+ Type ```:q!``` to quit without saving (You can't use ```:q``` when you have made changes).
+ Vim can be a handful to get used to. Here's a couple of additional resources.
	+ [Here](http://www.tldp.org/LDP/intro-linux/html/sect_06_02.html) is a boring vim tutorial.
	+ [Vim Adventures](http://vim-adventures.com/) is a game that will get you aquainted with navigating vim.

### Other Useful Commands

+ cp - Copy
+ mv - Rename/Move
+ touch - Create file/Update timestamp
+ which - View location of command/sanity check if command is installed
+ man - Open Manual Entry for a Command (press ```q``` to exit)
+ clear - Clears terminal window
+ history - Print history of commands run in terminal
+ cat - Print contents of file/stream
+ head - Print first number of lines in a file/stream
+ tail - Print last number of lines in a file/stream
+ grep - Filter contents of a file/stream
+ chmod - Change File Mode
+ ps - Show active Process Status
