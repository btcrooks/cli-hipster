# cli-hipster  
Cheat sheet of common bash/shell commands.  
This cheat sheet is intended for **Mac OS X** users. Some commands may differ on Linux.  
Note: `$` denotes the terminal prompt. Do **NOT** type them as part of your code.

## Navigation  
###### Change Directory  
    $ cd <directory>
###### User/Desktop  
    $ cd ~/Desktop
###### Up one level  
    $ cd ../
###### Navigate to home directory
    $ cd
    
## Managing Directories and Files
###### List Directories  
    $ ls
###### View Current Working Directory  
    $ pwd

### Copy
###### File
    $ cp file.txt
###### Directory
    $ cp path/to/directory

### Move
###### File
    $ mv file.txt new_dir/file.txt
###### Directory
    $ mv directory /new/directory

### Rename
###### File
    $ mv file.txt new.txt
###### Directory
    $ mv directory new_directory_name

### Delete
###### File
    $ rm file.txt
###### All Text Files
    $ rm *.txt
###### Directory
    $ rm -rf directory/

### Create  
###### Create an empty file  
    $ touch file.txt
###### Create a file with text  
    $ echo "Some text here" > some_file.txt
If the file name exists, bash will overwrite the existing file with the new text. To **append** data to an existing file, use double cheverons `>>`.  
Example: `$ echo "New text to append." >> existing_file.txt`

###### Directory  
    $ mkdir directory_name
To create a new directory with spaces in the file name, use back slashes `\` to escape each spaces.  
Example" `$ mkdir directory\ with\ spaces`  

### View
###### View contents of a file containing plain text.
    $ less file.txt
Press `q` to exit less. Use `more` or `cat` to display file contents within the prompt window.  
Example: `$ more file.txt`


### Search
###### Search for directories  
    $ find /path/to/search "Directory_Name"  
###### Search for files within a directory
    $ find /path/to/search -iname "File_Name"
Search for all files ending with **.txt** on the **Desktop**  
Example: `$ find ~/Desktop -iname "*.txt"`  
Note: Use `-name` to match case exactly. Use `-iname` to ignore case altogether.  
  
List all files in current and sub directorie(s)  
Example: `$ find .`  
###### Search within files
    $ grep -r 'Search string' path/to/search
Search for files containing `Hello World` on the desktop and return results in color.  
Example: `$ grep -r --color 'Hello World' ~/Desktop`  
###### Search
    $ mdfind

### System Processes
###### View all running processes live
    $ top  
###### Display all running processes
    $ ps aux
Display all processes and pipe into `less`  
Example: `$ ps aux | less`  
  
Display processes, pipe into `grep` searching for processes that start with sys and pipe into `less`.  
Example:  `$ ps aux | grep sys* | less`  

## Shortcuts & Tips  
###### Last command  
    [Up Arrow]
###### Autocompletion  
    [tab]
###### Clear inputted text
    [ctrl + U]
###### Delete Word (forward)
    [esc + D]
###### Delete Word (backward)
    [ctrl + W]
###### Home Directory  
    "~/"
###### Prepend Previous Command  
    $ <command> !!
###### Append Previous Command
    $ !! <command>


# Roadmap
* Table of Contents
* How to use Man Pages
* How to use wildcards `*`
* How to use regular expressions  
