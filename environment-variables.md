The Environment Variables are variables that store information about the user and the device.

How you can get the Environment Variables?

==Answer:== you can run this command in the terminal:

env


You will get all environment variables.

Examples:
PWD  = /home/kali/Desktop
USERNAME = kali
HOME = /home/kali
USER = kali
LANG = en_US.UTF-8
PATH  -----> (later)
SHELL -----> (later)


You can print the Environment Variables using bash commands like this:

echo $PWD


→ prints the assigned value of PWD (for example: /home/kali/Desktop)

echo $LANG


→ prints the assigned value of LANG (for example: en_US.UTF-8)

Path & Shell
Path

How does the device know that the command you run is a valid command?

The system searches for your command inside the directories stored in the PATH variable.

echo $PATH


Example output:

/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games


These directories contain the commands you can use.

You can edit the PATH (temporary for the current session):

Append (add a new path):

export PATH=$PATH:/your/new/path


Change the PATH completely:

export PATH=/path1:/path2:/path3

Shell

The shell is the program that executes your commands inside the terminal.

The environment variable SHELL stores the type of shell you are using.

Shell types: Bash, SH, Dash, Csh, Zsh.

To know the shell you are using now:

echo $SHELL


To start another shell temporarily:

zsh


To exit the current shell:

exit
