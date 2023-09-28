## Day 2 - Scripting

- `mkdir` - make new directory/file
- `cd ..` - go back one file
- `mv` - can rename but also move 
- `mv <filename> <what folder to send to>` - move the file to another folder


### Scripting
1. `nano provision.sh - creating script with shell extension
2. control + X = save and exit files
    
####  Copy and Paste

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
