# cli-hipster  
###### Cheat sheet of common bash/shell commands.
Although these commands work across linux distro's, this cheat sheet was intended for **Mac OS X** users.

## Navigation  
###### Change Directory  
    $ cd <directory>
###### User/Desktop  
    $ cd ~/Desktop
###### Up one level  
    $ cd ../

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
    $ mv file.txt /new_dir/file.txt
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
If the file name exists, bash will overwrite the existing file with the new text. To **append** data to an existing file, use a double cheveron `>>`.  
Example: `$ echo "New text to append." >> existing_file.txt`

###### Directory  
    $ mkdir directory_name
To create a new directory with spaces in the file name, use back slashes `\` to escape each spaces.
Example" `$ mkdir directory\ with\ spaces`

### View
###### View contents of a file containing plain text.
    $ less file.txt
press `q` to exit less

### Search
###### Search for files within a directory
    $ find <dir> -iname "Search Term"
Example: Search for all files ending with **.txt** on the **Desktop**
`$ find ~/Desktop -name "*.txt"`
##### Search
    $ mdfind

## Misc  
###### Last command  
    [Up Arrow]
###### Autocompletion  
    [tab]  
###### Home Directory  
    "~/"
###### Prepend Previous Command  
    $ <command> !!
###### Append Previous Command
    $ !! <command>

# Roadmap
* Using Man Pages
