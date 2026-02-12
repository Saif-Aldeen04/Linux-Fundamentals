# SU Command

#### SU: stands for **Switch User**.

`su`

→ Switches your user to **root**, but it asks you to enter the **root password** first.

`su testuser`

→ Switches your user to **testuser**, and asks for the password of **testuser**.

---

## SU with Login Environment

SU can also switch to another user with a similar environment as if the user logged in directly.

`su -`

→ Switches to **root** with root’s full login environment.

`su - testuser`

→ Switches to **testuser** with testuser’s full login environment.

The `-` loads the user’s environment variables (like HOME, PATH, etc.).

---

## Run a Command Without Full Shell

SU can also run a single command without opening a full shell:

`su username -c command`

Example:

`su testuser -c whoami`

or

`su - testuser -c whoami`

Output:

`testuser`

---

# Sudo Command

Try this command:

`cat /etc/shadow`

Output:

`cat: /etc/shadow: Permission denied`

This happens because the file requires root privileges.

---

## Sudo: Run Single Command as Root

`sudo cat /etc/shadow`

Now you can see the output.

By default, `sudo` asks for **your own password**, not the root password.

---

## Get Full Root Shell

`sudo -i`

→ Opens a full root shell.

You do not need to enter the root password, only your own password (if your user has sudo privileges).
