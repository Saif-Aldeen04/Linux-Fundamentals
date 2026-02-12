## 1️⃣ Definition

Built-in commands are commands that are part of the shell itself.

- They execute faster because they do not need to start a new process.
    
- They are handled directly by the shell (Zsh or Bash).
    

---

## 2️⃣ Common Examples

- `cd`
    
- `echo`
    
- `pwd`
    
- `exit`
    
- `export`
    
- `history`
    

---

## 3️⃣ How to Check if a Command is Built-in

> [!IMPORTANT]  
> Use the `type` command to check whether a command is built-in or external.

### Standard Usage

`type command_name`

### Example

`type cd`

Output:

`cd is a shell builtin`

---

## 4️⃣ How to Get Help or Details About Built-in Commands

### 📘 Method 1: Read the Shell Manual

You can open the shell manual page:

`man bash`

Since built-in commands are part of the shell, their documentation is included in the shell manual.

You can search inside the manual by pressing:

`/command_name`

Example:

`/cd`

Press `n` to go to the next match.

---

## 🔎 Alternative Help Method

Some shells also support:

`help command_name`

Example:

`help cd`

> [!IMPORTANT]  
> The `help` command works for shell built-ins but may not work for external commands.
