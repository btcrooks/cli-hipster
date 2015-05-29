# cli-hipster  
Cheat sheet of common bash/shell commands  

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
###### File  
    $ touch file.txt
###### Directory  
    $ mkdir directory_name
###### Directory with spaces in the file name
    $ mkdir directory\ with\ spaces
### Search
###### Search for files within a directory
    $ find <dir> -iname "Search Term"
 - Example: Search for all files ending with **.txt** on the **Desktop**
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
