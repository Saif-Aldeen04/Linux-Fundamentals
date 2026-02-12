
## Update Repository (Always Run First)

To install software in Linux (Debian-based systems), you usually do not download it from the official website.

Linux uses **repositories** (servers that contain thousands of software packages).

When you update, you refresh the package list (cache) of your system.

- Update command:
    

`apt-get update`

This command updates the local package index.  
It does NOT upgrade software, it only updates the list.

---

## Upgrade All Software

This command upgrades all installed software on your system:

`apt-get upgrade`

---

## Upgrade Including Kernel and Dependencies

`apt-get dist-upgrade`

This command upgrades software and also handles dependencies.  
It may install or remove packages if needed.

---

## Run Update and Upgrade Together

`apt-get update && apt-get dist-upgrade`

Here we use `&&` to run the second command only if the first command runs successfully.

---

## Install / Remove Software

- To install:
    

`apt-get install software_name`

- To remove:
    

`apt-get remove software_name`

---

## Search for Software

`apt-cache search software_name`

This command searches for packages in the repository.

