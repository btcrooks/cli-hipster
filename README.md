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
```bash
$ cd
```

## Managing Directories and Files
###### List Directories  
```bash
$ ls
```
###### View Current Working Directory  
```bash
$ pwd
```

### Copy
###### File
```bash
$ cp file.txt
```
###### Directory
```bash
$ cp path/to/directory
```

### Move
###### File
```bash
$ mv file.txt new_dir/file.txt
```
###### Directory
```bash
$ mv directory /new/directory
```

### Rename
###### File
```bash
$ mv file.txt new.txt
```
###### Directory
```bash
$ mv directory new_directory_name
```

### Delete
###### File
```bash
$ rm file.txt
```
###### All Text Files
```bash
$ rm *.txt
```
###### Directory
```bash
$ rm -rf directory/
```

### Create
###### Create an empty file
```bash
$ touch file.txt
```
###### Create a file with text
```bash
$ echo "Some text here" > some_file.txt
```

If the file name exists, bash will overwrite the existing file with the new text. To **append** data to an existing file, use double cheverons `>>`.  
Example: `$ echo "New text to append." >> existing_file.txt`

###### Directory
```bash
$ mkdir directory_name
```
To create a new directory with spaces in the file name, use a back slash **`\`** to escape each spaces.  
Example: `$ mkdir directory\ with\ spaces`  

To create a new directory and cd to that directory in one shot, use
```bash
$ mkdir new_directory && cd new_directory

# or use the most recent parameter variable: $_

$ mkdir new_directory && cd $_
```

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
Note: Use `-name` to match case exactly. Use `-iname` for case insensetive search.  

Search for all files ending with **.txt** on the **Desktop**  
Example: `$ find ~/Desktop -iname "*.txt"`  
  
List all files in current and sub directorie(s)  
Example: `$ find .`  
###### Search within files
    $ grep -r 'Search string' path/to/search
Search for files containing `Hello World` on the desktop and return results in color.  
Example: `$ grep -r --color 'Hello World' ~/Desktop`  
###### Search
```bash
$ mdfind
```
### System Processes
###### View all running processes live
```bash
$ top
```
###### Display all running processes
```bash
$ ps aux
```
Display all processes and pipe into `less`  
Example: `$ ps aux | less`  
  
Display processes, pipe into `grep` searching for processes that start with sys and pipe into `less`.  
Example:  `$ ps aux | grep sys* | less`  

## Shortcuts & Tips
###### Keyboard commands
Note: `⌃` denotes the control button.  

Last command: `⇧  ( Up Arrow )`  
Autocompletion: `TAB`  
Clear inputted text: `⌃u`  
Delete Word (forward): `ESC + d`  
Delete Word (backward): `⌃w`  
Find previously used commnad: `⌃r`  

###### Bash Commands
Home Directory: "~/"  
Prepend Previous Command: `$ <command> !!`  
Append Previous Command: `$ !! <command>`  
Send items to your clipboard: `$ <command> | pbcopy`  
Get items from your clipboard: `$ pbpaste > file.txt`  

## [NPM - Node Package Manager](https://www.npmjs.com/)
###### List Installed Packages, sans dependency tree.
```bash
$ npm ls --depth=0
```
Use the `-g` flag for globally installed packages.  

# Roadmap
- [ ] Table of Contents
- [ ] How to use Man Pages
- [ ] How to use wildcards `*`
- [ ] How to use regular expressions
- [ ] How to do basic customization {i.e .bash_profile}
