Analyzing the structure of the /etc/passwd and /etc/group:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/1.png

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/2.png

In this files we can see pseudo-users and users, like roots and administators.
We can define pseudo-user by analyzing setting configuration for exists users : pseudo users are pre-defined users such as 'mail', 'uucp, 'nobody', etc...


A UID (user identifier) is a number assigned by Linux to each user on the system.
This number is used to identify the user to the system and to determine which system resources the user can access.
We can define user`s UID by analyzing information about current processes (ps -a) or by using command ls -l, which outputing data, which include information about users and thems UID.


GUI - identify group by a group identifier, that used to determine which system resources a user or group can access.
We can define user`s GID as well as determine him UID.


We can determine belonging of user to the specific group by analyzing results of command group *NameOfUser*


We can add user by using command useradd:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/3.png


We can rename or change name of user by using a usermod command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/4.png


The /etc/skel directory contains files and directories that are automatically copied over to a new user’s when it is created from useradd command.
This will ensure that all the users gets same intial settings and environment.

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/5.png


We can delete a user account and all its associated files using the userdel command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/6.png



To lock and unlock a user account, we can use command passwd -l, which in result lock a user account, and passwd -u for unlocking a user account.

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/7.png

Or by using a command usermod with similar operators:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/8.png


To provide users with a password-free login, we can use command usermod:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/9.png


To display the extended format of information about the directory, we need to use ls command:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/10.png

In that columns we can find information about permissions for acces, owner`s UID, name of file and the last date and time of change this file.


Access rights in Linus OS - it`s sequence of three columns, which specified access for user, group, other users to current file or directory.
That sequence can list three symbols of access rights: 
"r" - read - that in octal representation have 4 bits - give to user/group/other users access rights to read a file or directory with files.
"w" - write - that in octal representation have 2 bits - give to user/group/other users access rights to change information in files on certain directory.
"x" - execute - that in octal representation have 1 bit - give to user/group/other users access rights to execute some actions with certain directory or file (for example, deleting, creatin,moving files).
Access rights can tell about the relationship between the file and the user.


The chmod and chown commands are used to change the mode of acces to the file and to change the owner of file:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/13.png

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/14.png


Describing umask command with example of octal representation of access rights:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/11.png


Sticky bit is a user ownership access right flag that can be assigned to files and directories.
If you set the sticky bit to a directory, other users cannot delete or rename the files (or subdirectories) within that directory.
When the sticky bit is set on a directory, only the owner and the root user can delete / rename the files or directories within that directory.
Example of using sticky bits:

https://raw.githubusercontent.com/Azizman1/DevOps_online_Lviv_2020Q42021Q1/main/Task%205.2/12.png
