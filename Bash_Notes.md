# writing bash scripts

.sh extension
command line arguments
e.g. -l , /etc are command line arguments of ls

to run: either bash myscript.sh, /home/me/myscript.sh, ./myscript.sh


#!/bin/bash - shebang - includes the path to the interpreter that should be used to run the rest of the lines in the file. 
-shebang will be to bash for all bash programs, but every script type has its own interpreter. 

### process = running instance of a program
running/executing the script: 

### $PATH variable = individual user variable
many different versions of a program can be installed
absolute path- includes all directories and files in the path
e.g. /home/me/script.sh

## Absolute and Relative Paths

## referencing paths in the command line
   - tilde-  this is a shortcut for the home directory
   . dot- reference to teh current directory
   .. dot dot- reference to parent directory. ../../ lists root directory

 
## setting variables:
e.g. variable=value

## command substitution:
myvar=$( ls )


## Exporting Variables

### scope - each variable is limited to the process they were created in. If we want to use the variable in more than one script, we need to export


## LINUX - 
case sensitive
extensionless (in order to see file extension you need to use file mydirectory)
hidden files -a


## Manual Pages:
Searching Manual pages: 
man -k <search term>
or hit / followed by term you wish to search then enter
scroll through multiple entries with "n" key
File Navigation:
listing files: ls 
options:
-l lists the access codes, the date of last modification, the user code, the size and the name
-a lists all the files and directories, including those beginning with . 
-t lists the files and directory in order of when they were last modified
File Manipulation:
directory creation:
mkdir [options] <Directory>
useful options:
-p creates parent directories as needed
-pv creates parent and prints outcome

## file removal:
rmdir [options] <Directory> 
-p removes parent directories as needed
-v 

## blank file:
touch [options] <filename>

## copying a file or directory:
   cp [options] <source1><source2>...<source n><destination>
   *many options:* 
   -r = recursive. looks at a directory and all files and directories within in, and for subdirectories go into them and do the same thing and keep doing this.

copying all files of a certain name - cp *.txt <destination> or cp m*.txt <destination> 
* is called wildcard. it will select all files in the working directory


## moving a file:
   mv [options] <source> <destinations>
   we can rename a file by including a destination name
   * e.g. mv foo2 backups/foo3 <- here we moved the file foo2 to backups directory under a new name "foo3"
   * e.g. 2 mv superman.txt batman.txt <--- this overwrites superman.txt to a new file of name "batman.txt"

Copy vs. Move
- use move to rename a file (the first file argument will be deleted and renamed to the second argument. ** this command will overwrite the contents of the destination file, or create a new file by that name if none currently exists. 
- use copy to rename a file and keep a copy of it with its original name. Good for version control! But, copy will overwrite the contents of the destination file name, so be careful not to overwrite a file you need. 


## renaming a file or directory:
e.g. mv linuxtutorialwork/testdir /home/me/linuxtutorialwork/fred
here, we moved renamed the file testdir to be named fred

## remove a file:
rm [options] <file> 
rm -r  - this will removed a file and all its contents
rm <directory>/* - this removes all files within a directory


## I/O
cat- reads the contents of a file
echo - prints the following argument to standard output
command [file1] > [file2] redirects output to <file>
less- similar to echo, but prints long files one page at a time.
options -N adds line numbers to a file
wc counts the words and characters
sort orders them alphabetically
uniq omits adjacent duplicate lines. 
grep "global regular expression print" searches for a pattern and prints entries matching the pattern.
grep [options] PATTERN file/directory
options : -i case insensitive 
-R searches all files in a directory for a certain term
sed - stream editor, similar to find and replace
options
s - substitution
snow-  search the string (text to be found)
rain- replacement string, text to add in one place
e.g. sed 's/snow/rain' rainforests.txt - all instances of snow are replaced with rain
history - prints the last 10 commands used 

nano text editor- based on Pico UW model of text 
invoke with the  nano [file name] 
to access variables and commands set in a nano file, use source [file name] command

Environmental Variables:
used across programs and commands and store information about the environment. 
write them with the variable name
access them with $
USER- stores name of user
PS1 - defines the makeup and style of the command line prompt
HOME- displays the path of the home directory
PATH- stores a list of directories separated by a colon. these directories contain scripts for the command line to execute


## env- prints the environmenal varial

## piping:
command to command redirection


## shortcuts:
mkdir vue-cdn && vue-cdn -this makes the folder and enters it too. 

##bash profile:
.bash_profile - stores aliases, 


