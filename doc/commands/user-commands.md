# User commands

## Summary
- [chmod](#chmod)
- 

## chmod
To grant specific file permission to a user or group, specify the user (u) or group (g), followed by the permission attribute and the file name.
The syntax is as follows:
```
chmod [entity + permissions] [file]
```
## chgrp
To change groups of files and directories in Linux. 
```
chgrp groupname filename
```
```
chgrp groupname foldername
```
## chown
To change ownerships of files and directories in Linux:
```
chown name filename
```
```
chown name foldername
```
## useradd
To create a regular user using the useradd command following this syntax:
```
useradd -m <name-of-user>
```
## usermod
To assign admin privileges to this user as follows:
```
usermod -aG sudo <username>
```
## sudo su
To switch to the admin superuser using the following command:
```
$ sudo su <adminuser>
```
## sudo useradd
To create more users with the useradd command:
```
$ sudo useradd -m <name of user>
```
