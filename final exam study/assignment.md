---
Name: Sayma Akter
Course: CIS106
Semester: Fall 2022
---

# Question 1

## awk
 * Description:
   * awk is a scripting language used for processing and displaying text. Awk can work with a text file or from standard output. Awk was created in Bell Labs during the 70s by Alfred Aho. Peter Weinberger, and Brian Kernighan and its name comes from its authors' initials. There are several implementations Awk: nawk, mawk, gawk, and busybox. 
   * Awk performs operations line by line
 * Formula:
   * `awk + options + {awk command} + file + file to save (optional`       
   * `command output` | `awk + options + {awk command}`

* Examples: 
  * How to print the first field of a file:
    * `awk -F: '{print $1}' /etc/passwd`
  * print the last field of the /etc/passwd file
    * `awk -F: '{print $NF}' /etc/passwd`
  * Print the first and last field of the /etc/passwd
    * `awk -F: '{print $1," = ",SNF}' /etc/passwd`

## cat
  * Description:
    * The cat command is used for displaying the content of a file
    * Cat is short for concatenate which is its command intended use.
  * Syntax/Formula:
    * `cat + option + file or files to view/concatinate`
  * Examples:
    * How to see the content of a file
      * `cat /etc/passwd`
    * How to see the content of a file with line numbers:
      * `cat -n /etc/passwd`
    * How to see the content of a file with ending line character 
      * `cat -E /etc/passwd`

## cp
  * Description:
    * cp copies files/directories from a source to a destination
  * Syntax/Formula:
    * the cp command uses the same structure as the mv command
        * `cp + files to copy + destination`
  * Examples:
      * to copy directories you must use the -r option
        * `cp -r + directories to copy + destination`
    * to copy a file 
        * `cp Downloads/wallpapers.zip Pictures/`
    * to copy a directory with absolute path
        * `cp -r ~/Downloads/wallpapers ~/Pictures/`
    * to copy the content of a directory to another directory 
        * `cp Downloads/wallpapers/* ~/Pictures?`

## cut
  * Description:
    * The cut command is used to extract a specific section of each line of a file and display it to the screen
  * Syntax/Formula:
    * `cut + option + file (s)`
  * Examples:
    * Display a list of all the users in your system
      * `cut -d ':' -f1 /etc/passwd`
    * Display a list of all the users in your system with their login shell
      * `cut -d ':' -f1,7 /etc/passwd`
    * Cut a range of bytes per line
      * `cut -b 1-5 usernames.txt`

## grep
  * Description:
    * Grep is used to search text in given file. Grep works line by line basis (it matches the search criteria in a line by line basis)
  * Syntax/Formula:
    * `grep + option + search criteria + file (s)`
  * Examples:
    * Search any line that contains the word "dracula" in the given file:
      * `grep 'dracula' ~/Documents/dracula.txt`
    * Search and match only the word
      * `grep -o 'dracula ~/Documents/Books/dracula.txt`
    * Search for a given strings inside files in a given directory
      * `grep -iR 'conf' /etc/`
  
## ls
  * Description:
    * ls is used for listing the content of a given directory or the file/directory itself
  * Syntax/Formula:
    * `ls + option + directory to list`
  * Examples:
    * list the content of the present working directory
      * `ls`
    * list all the files inside the current working directory including hidden files
      * `ls -a`
    * list all the files inside a given directory
      * `ls -a ~/Pictures`

## man
* Description:
  * man (manual) pages are documentation files that describe Linux shell commands, executable programs, system calls, special files, and so forth.
* Syntax/Formula:
  * `man ls`
* Examples:
  * open the man page of the passwd command
    * `man passwd`
  * open a specific man page for the passwd command
    * `man 5 passwd`
  * show man the man page section of the passwd command
    * `man -f passwd`

## mkdir 
 Description:
  * mkdir is used for creating a single directory or multiple directories 
* Syntax/Formula:
  * to create a directory with mkdir use the following formula 
    *  `mkdir + the name of the directory`
* Examples:
  * Create a directory in the present working directory
    * `mkdir wallpapers`
  * Create directory in a directory using relative path
    * `mkdir wallpapers/ocean`
  * Create directory in a different directory using absolute path
    * `mkdir ~/wallpapers/forest`
## mv
* Description:
  * mv moves and renames directories 
* Syntax/Formula:
  * the basic formula of the mv command is:
    * `mv + source + destination`
* Examples:
  * For renaming files/directories the formula remains same
    * `mv + file/directory to rename + new name`
  * To move a file a directory to another using relative path
    * `mv Downloads/homework.pdf Documents/`
  * To move a directory from one directory to another using absolute path
    * `sudo mv ~/Downloads/theme /usr/share/themes`
## tac
* Description:
  * The tac command is used for displaying the content of a file in reverse order.
  * Just like cat, tac concatenates files and displays the output of the concatenation
* Syntax/Formula:
  * `tac + option + file(s) to display`
* Examples:
  * Display the content of a file located in the pwd
    * `tac todo.md`
  * Display the content of a file using absolute path
    * `tac ~/Documents/todo.md`

## head
* Description:
  * The head command displays the top N number of lines of a given file. By default, it prints the first 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
* Syntax/Formula:
  * `head + option + file (s)`
* Examples:
  * Display the first 10 lines of a file
    * `head ~/Documents/Books/dracula.txt`
  * Display the first 5 lines of a file
    * `head -5 ~/Documents/Book/dracula.txt`
  
## tail
* Description:
  * The tail command displays the top N number of lines of a given file. By default, it prints the first 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
* Syntax/Formula:
  * `tail + option +file`
* Examples:
  * Display the first 10 lines of a file
    * `tail ~/Documents/Book/dracula.txt`
  * Display the first 5 lines of a file
    * `tail -5 ~/Documents/Book/dracula.txt`