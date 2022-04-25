task-01.md

* Create 3 groups and 15 users
* Assign the 15 users across the 3 groups
* Demonstrate that user(s) in a group cannot access files/folders that belong to another group unless they are added to that group

Commands to achieve the taks:
```
All commands by the root user
create a new user : adduser user1
- type in the command /etc/passwd -to check if 'user1' was created

create a group : groupadd group1

add 'user1' to 'group1' : usermod -g group1 user1

create a directory #in the file /usr : mkdir /usr/folder4grp1only
-type ls -l /usr : to see the list of files in the directory in the long list format
 
change the default group of the directory from root to group1 : chgr group1 /usr/folder4grp1only

change the permission of the file to rwx for the owner and rwx for the other group1 members: chmod 770 /usr/folder4grp1only
 
create 4 more users and assign to group1
do the same for group2 and 3

to test 
su user2
cd /usr/folder4grp1only/hello.txt ##permission should be denied
```
