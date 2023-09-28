## Deploying Nodejs App

1. Create instance on AWS called this "tech254_wafa_testapp". When creating the instance,Select an existing group instead of creating one.
![](C:\Users\wafam\Documents\Tech_254\Linux\network_settings.png)
2. Click into the Instance and scroll down to **Security**
3. Click onto the "Security Group" link shown below to edit the Inbound Rules
![](C:\Users\wafam\Documents\Tech_254\Linux\security_group_link.png)
4. Click **Edit Inbound Rules**
5. Add Rule > Custom TCP 
6. Port Range = `3000`
7. Source = `Anywhere-IPv4`
8. **Save Rules**

Instance has been created on AWS.

#### Copy files 
9. Open Gitbash Terminal
10. go into Tech_254 folder by `cd Documents`, `cd Tech_254`
11. Run command `ls` to make sure you're in Tech_254
12. Run command `scp -i "C:/Users/wafam/.ssh/tech254.pem" -r app ubuntu@ec2-54-73-123-26.eu-west-1.compute.amazonaws.com:~`
NOTE: this will take 5 minutes to copy all the files 

13. When files have finished copying, connect te Instances.
14. run command `cd` to take you to home directory 
15. Run command `cd .ssh` to be inside the ssh folder
14. Run command `chmod 400 tech254.pem`
15. Run Command `ssh -i "tech254.pem" ubuntu@ec2-34-245-219-171.eu-west-1.compute.amazonaws.com`
16. Should be connected to instance

17. Run command `git clone https://github.com/LSF970/sparta_test_app.git`
18. Run command `cd sparta_test_app` to go into the file that was cloned
19. Run `ls` command to see if app is in there
20. `cd app` go into the app folder
21. Run command `curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`
22. Run command `sudo apt install nodejs -y`
23. Run command ```node -v``` to see which version. Should output v12.22.12
24. Run command `sudo npm install pm2 -g`
25. Run following command 
```
npm install
```
26. To see if it is successful and working, run command
```
node app.js
```
