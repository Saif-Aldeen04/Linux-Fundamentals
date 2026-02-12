
Before using commands, you should understand the concept of **options** in the shell.

Options are written like this:

> [!info]  
> Command -Option

An option gives you more control or more information about the command.

You can combine options like this:

> [!info]  
> Command -OptionOption

You can get help and see available options by writing `--help` after most commands:

> [!info]  
> Command --help

---

##### 1. **ls**

**Definition:** List files and directories.

- You can give a specific path to list files in that location.
    
- Some options:
    
    - `-a` : List all files (hidden and unhidden).
        
    - `-l` : Long list format.
        
    - `-al` : List all files in long format.
        

---

##### 2. **cd**

**Definition:** Change current directory.

Arguments:

- `Path` : Move to a specific directory.
    
- `..` : Go to parent directory.
    
- `.` : Stay in the current directory.
    

If you run `cd` without arguments, it will move you to your home directory (for example `/home/kali` in Kali Linux).

---

##### 3. **clear**

**Definition:** Clear the terminal screen.

---

##### 4. **pwd**

**Definition:** Print Working Directory.  
Displays your current directory.

---

##### 5. **cp**

**Definition:** Copy files or directories.

Copy file to another path:  
`cp a.txt /home`

Copy and rename in same directory:  
`cp a.txt b.txt`

---

##### 6. **mv**

**Definition:** Move or rename files and directories.

Rename:  
`mv Old_Name New_Name`

Move:  
`mv file_name Path`

---

##### 7. **man**

**Definition:** Display manual page for a command.

Example:  
`man ls`

To read about `man` itself:  
`man man`

> [!info]  
> Some commands are built-in commands, so `man` may not show full help for them.

[[Built-in Commands]]

---

##### 8. **touch**

**Definition:** Create an empty file.

`touch a.txt`

---

##### 9. **mkdir**

**Definition:** Create directory.

`mkdir test`

Directory with spaces:  
`mkdir "My directory"`

---

##### 10. **rmdir**

**Definition:** Remove empty directory.

`rmdir test`

---

##### 11. **rm**

**Definition:** Remove files or directories.

Remove file:  
`rm file_name`

Option:

- `-r` : Remove directory recursively.  
    `rm -r directory_name`
    

---

##### 12. **cat**

**Definition:** Display file content.

---

##### 13. **nano**

**Definition:** Terminal text editor.

`nano file_name`

---

##### 14. **grep**

**Definition:** Search for text inside files.

Example:  
`grep "word" a.txt`

Displays all lines containing the word.

---

##### 15. **head**

**Definition:** Display first 10 lines of a file.

Option:

- `-n` : Specify number of lines.  
    `head -n 7 a.txt`
    

---

##### 16. **tail**

**Definition:** Display last 10 lines of a file.

Options:

- `-n` : Specify number of lines.
    
- `-f` : Monitor file changes in real time.
    

`tail -n 7 a.txt`

---

##### 17. **less**

**Definition:** Display file content page by page.  
Press `Enter` or `Space` to continue.

---

##### 18. **ps**

**Definition:** Display running processes.

Option:

- `aux` : Show all processes on the system.  
    `ps aux`
    

---

##### 19. **lsof**

**Definition:** List open files.

Option:

- `-i` : Show network-related open files.  
    `lsof -i`
    

---

##### 20. **netstat**

**Definition:** Display network connections.

Options:

- `-a` : All connections.
    
- `-n` : Show IP addresses instead of domain names.
    
- `-t` : TCP only.
    
- `-u` : UDP only.
    
- `-p` : Show PID and program name.
    

Example:  
`netstat -antp`

---

##### 21. **ifconfig**

**Definition:** Display network interface information.

Shows:

- IP address
    
- MAC address
    
- Subnet mask
    
- Broadcast address
    

---

##### 22. **ping**

**Definition:** Test network connectivity.

You can use IP address or domain name.  
Example:  
`ping google.com`

---

##### 23. **curl**

**Definition:** Transfer data from or to a server (HTTP, HTTPS, FTP, etc.).

View response:  
`curl https://example.com`

Download file:  
`curl -O https://example.com/file.txt`

---

##### 24. **wget**

**Definition:** Download files from the internet.

Download file:  
`wget https://example.com/file.txt`

Resume download:  
`wget -c https://example.com/file.txt`

---

##### 25. **sort**

**Definition:** Sort file content alphabetically.

`sort a.txt`

Save sorted output:  
`sort a.txt > sorted_file`

---

##### 26. **uniq**

**Definition:** Remove duplicate lines (file should be sorted first).

`uniq sorted_file > uniq_file`

---

##### 27. **stat**

**Definition:** Display detailed file information.

`stat a.txt`

---

##### 28. **whoami**

**Definition:** Display current user.

---

##### 29. **passwd**

**Definition:** Change user password.

The system will ask for:

- Old password
    
- New password (twice)
    

---

##### 30. **kill**

**Definition:** Terminate a process.

`kill 1720`

Use `ps` to get the process ID.

---

##### 31. **find**

**Definition:** Search for files in a specific path.

`find path -name "file_name"`

Search entire system:  
`find / -name a.txt`

---

##### 32. **ln**

**Definition:** Create links.

Hard link:  
`ln file_name link_name`

Symbolic link:  
`ln -s file_name link_name`
