# User commands

## Summary
- [chmod](#chmod)
- [chgrp](#chgrp)
- [chown](#chown)
- [useradd](#useradd)
- [usermod](#usermod)
- [sudo su](#sudo-su)
- [sudo useradd](#sudo-useradd)
- [getent passwd](#getent-passwd)
- [sudo userdel](#sudo-userdel)
- [sudo groupadd](#sudo-groupadd)
- [sudo gpasswd](#sudo-gpasswd)
- [getent group](#getent-group)

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
## getent passwd
To view all users, run the following command:
```
$ getent passwd
```
## sudo userdel
To delete a user, run the command:
```
$ sudo userdel -f <user>
```
## sudo groupadd
To create a group, run the following command:
```
$ sudo groupadd <groupname>
```
## sudo gpasswd
To add an already created users to each group assuming each user fits the group role, use the gpasswd command with the following syntax:
```
$ sudo gpasswd -A <user> -M <user,user,user> <groupname>
```
## getent group
To view all groups, run the following command:
```
$ getent group
```