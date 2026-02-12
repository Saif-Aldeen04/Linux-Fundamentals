There are special characters in Linux that have specific meanings inside the shell.

**Special characters:** Characters that perform special actions in the shell instead of being treated as normal text.

---

## / (Slash)

It is called the **directory separator**.

Example:

`cd home/student/Desktop/Pentest`

The slash `/` is used to separate directories in a path.

---

## \ (Backslash)

It is called the **escape character**.

It cancels the special meaning of the next character and treats it as normal text.

#### Example 1: Escaping Spaces

In Linux, space is used to separate arguments.

If you want to create a directory called:

`hello hacker`

You must escape the space:

`mkdir hello\ hacker`

The backslash `\` cancels the special meaning of space.

#### Example 2: Escaping the Star (\*)

In Linux, the star `*` is a wildcard (special character).

Example:

`find *.txt`

This command finds all files that end with `.txt`.

If you want to create a directory literally called:

`*.txt`

You must escape the star:

`mkdir \*.txt`

---

|Command|Meaning|
|---|---|
|`find *.txt`|Get all files with extension `.txt`|
|`find \*.txt`|Search for a file literally named `*.txt`|

---

## . (Dot)

Represents the **current directory**.

Example:

`cd .`

---

## .. (Two Dots)

Represents the **parent directory** (the directory above the current one).

Example:

`cd ..`

---

## ~ (Tilde)

Represents the **home directory of the current user**.

Example:

`cd ~`

This command moves you to your home directory.

---

## & (Ampersand)

Runs a program in the **background**.

Example:

`gedit &`

The program opens in a new window, and the terminal gives you a process ID.

---

## * (Star)

`*` is a wildcard.

It represents **zero or more characters**.

Example:

`ls *.txt`

Matches:

- a.txt
    
- file.txt
    
- notes.txt
    

---

## ? (Question Mark)

Represents **exactly one character**.

Example:

`ls a?.txt`

Matches:

- a1.txt
    
- ab.txt
    

Does NOT match:

- a17.txt
    

---

## [ ] (Square Brackets)

Used to represent a **range of characters**.

Examples:

`[0-9]   → from 0 to 9 [A-Z]   → from A to Z [a-z]   → from a to z`

Suppose we have these files:

`a17.txt a1.txt ad.txt aC.txt`

---

|Command|Output|
|---|---|
|`ls a[0-9].txt`|a1.txt|
|`ls a[0-9][0-9].txt`|a17.txt|
|`ls a[A-Z].txt`|aC.txt|
|`ls a[a-z].txt`|ad.txt|

One range = one character.

In `a[0-9][0-9].txt`:

- First range matches `1`
    
- Second range matches `7`
    

---

## Command Separators

You can run multiple commands in the same line using:

- `;`
    
- `&&`
    
- `||`
    

---

|Separator|How It Works|Example|Result|
|---|---|---|---|
|`;`|Run both commands regardless of result|`pwd ; whoami`|Always runs both|
|`&&`|Run second command only if first succeeds|`pwd && whoami`|Runs both if first succeeds|
|`||`|Run second command only if first fails|
