## Day 2 - Scripting

- `mkdir` - make new directory/file
- `cd ..` - go back one file
- `mv` - can rename but also move 
- `mv <filename> <what folder to send to>` - move the file to another folder


### Scripting
1. `nano provision.sh - creating script with shell extension
2. Copy and paste below
    
####  Copy and Paste
```
#!/bin/bash

#update
sudo apt update

#upgrade
sudo apt upgrade -y

#install nginx
sudo apt install nginx -y

#restart nginx
sudo systemctl restart nginx

#enable nginx
sudo systemctl enable nginx
```
3. `control + X, Y`, save file and exit 
4. `sudo +x nginx` - 
4. `./provision.sh` - run file 
5. `sudo systemctl status nginx` - check status is it is running 
6. Should get greet dot and 'Active'


### Linux Notes
- `ps` - processes running. Basic 
- `ps --help simple` - different commands for processes running
-  `-A, -e`               all processes
- ` -a`                   all with tty, except session leaders
- `-a`                   all with tty, including other users
- `-d`                   all except session leaders
- `-N, --deselect`       negate selection
-  `r`                   only running processes
-  `T`                   all processes on this terminal
-  `x`                   processes without controlling ttys
- `ps aux` - all the processes running 
- `top` - live processes running 
- `shift + M` - will rank live processes by memory used
- `Q` - exit and back to ubuntu user
- `kill -1 <PID NUMBER>` - kills processes running. USe this first
- `kill -15` - kills processing running
- `kill -9` or `kill -kill` - forceful kill. Big red button
- `chmod` - change permissions on file or folder
- 
