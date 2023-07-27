# Bash Scripting

## What Are Bash Scripts
A script is a file containing a series of commands.  The shell reads this file and carries out the commands as though they have been entered on the command line.  

## How to Write a Shell Script
<ol>
  <li>Write the script.</li>
  <li>Make the script executable.</li>
  <li>Put the script somewhere the shell can find it.</li>
</ol>

### Script File Format
<code>
#!/bin/bash
# This is our first script.
echo "Hello World!"
</code>

The #! sequence is a special construct called a <i>shebang</i>.  The shebang is used to tell the system the name of the interpreter that should be used to execute the script that follows.  Every shell script should include this as its first line.  The second line is a comment aimed at reminding you or anyone looking at your script what it does.  The last line is an <code>echo</code> command with a string argument.

### Executable Permissions
To make our script executable use the <code>chmod</code> command.  There are two common permission settings for scripts: 755 for scripts that everyone can execute and 700 for scripts that only the own can execute.  

## Script File Location 
The system searches a list of directories each time it needs to find an executable program, if no explicit path is specified.  The list of directories is held in an environment variable named PATH.  The PATH varialbe contains a colon separated list of directories to be searched.  You can view the contents of PATH:
<code>echo $PATH</code> 
If the script were located in any of those directories in the list the script would run.  Most Linux distributions configure the PATH variable to contain a bin directory in the user's home directory to allow users to execute their own programs.  
If the PATH variable does not contain the directory it can be easily added by including this line in the ~/.bashrc file <code>export PATH=~/bin:"$PATH</code>
