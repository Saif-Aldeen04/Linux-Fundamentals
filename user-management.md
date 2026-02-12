
You should be **sudo** to run these commands.  
You can use the word `sudo` before a command to get administrator privileges.

`sudo command`

---

## Create User

`useradd username`

If you want to create a user called **Saif**:

`useradd Saif`

---

## Set or Change User Password

`passwd username`

Example:

`passwd Saif`

---

## Create Group

`groupadd groupname`

Example:

`groupadd IT`

Here we create a group of users called **IT**.

---

## Add User to Group

`gpasswd -a username groupname`

Example:  
We want to add **Saif** to group **IT**:

`gpasswd -a Saif IT`

---

## Delete User

`userdel username`

Example:

`userdel Saif`

Here we delete the user called **Saif**.

---

## Delete Group

`groupdel groupname`

Example:

`groupdel IT`

---

# Important Files

---

## (/etc/passwd)

This file contains users and information about them.

`cat /etc/passwd`

It contains:

- Username
    
- Password placeholder
    
- User ID (UID)
    
- Group ID (GID)
    
- Comment (Full name)
    
- Home directory
    
- Shell type
    

Example output:

`root:x:0:0:root:/root:/bin/bash student:x:1000:1000:Student,,,:/home/student:/bin/bash`

Explanation:

- `:` → used to separate fields
    
- `root` / `student` → username
    
- `x` → password stored in another file (/etc/shadow)
    
- `0` / `1000` → User ID (root UID is always 0)
    
- Second `0` / `1000` → Group ID (root GID is always 0)
    
- `root` / `Student,,,` → full name
    
- `/root` / `/home/student` → home directory
    
- `/bin/bash` → shell type
    

---

## (/etc/shadow)

This file contains the hashed passwords of users.

It contains:

- Username
    
- Encrypted password
    

Example:

`cat /etc/shadow`

Example output:

`root:$6$fq5XQQCj$UHg4kUV643WdgGp6fSLXWLvy6h2Q3X9Rv1Yry8Ewb7lVUe02Eef7Rh6PqsiU.YrxcYfrIApmuiieq/n7qwGe.`

Encryption types:

- `$1$` → MD5
    
- `$6$` → SHA-512
    

---

## (/etc/group)

This file contains:

- Group name
    
- Group password (if exists)
    
- Group ID
    
- Members of the group
    

Example:

`cat /etc/group`

Example output:

`Scanner:x:119:saned,student`

Explanation:

- `Scanner` → group name
    
- `x` → no password
    
- `119` → group ID
    
- `saned,student` → users in this group
