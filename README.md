<h1>Manage authorization</h1>


<h2>Description</h2>
Use Linux commands to configure authorization.


<h2>Environments Used </h2>

- <b>Linux</b>
- <b>Bash Shell</b>

<h2>Scenario:</h2>

In this scenario, you must examine and manage the permissions on the files in the /home/researcher2/projects directory for the researcher2 user.

The researcher2 user is part of the research_team group.

You must check the permissions for all files in the directory, including any hidden files, to make sure that permissions align with the authorization that should be given. When it doesn't, you must change the permissions.

Here’s how you’ll do this task: 

<b>First</b>, you’ll check the user and group permissions for all files in the projects directory.

<b>Next</b>, you’ll check whether any files have incorrect permissions and change the permissions as needed.

<b>Finally</b>, you’ll check the permissions of the /home/researcher2/projects/drafts directory and modify these permissions to remove any unauthorized access.


<h2>Tutorial walk-through:</h2>

<h3>Task 1. Check file and directory details</h3>

In this task, you must explore the permissions of the projects directory and the files it contains. The lab starts with /home/researcher2 as the current working directory. This is because you're changing permissions for files and directories belonging to the researcher2 user.

1. Navigate to the projects directory.
2. List the contents and permissions of the projects directory.
   
The permissions of the files in the projects directory are as follows:

<img src="https://i.imgur.com/kZ4NOBb.png" height="80%" width="80%"/>

<h3>Task 2. Change file permissions</h3>

In this task, you must determine whether any files have incorrect permissions and then change the permissions as needed. This action will remove unauthorized access and strengthen security on the system.

None of the files should allow the other users to write to files.

1. Check whether any files in the projects directory have write permissions for the owner type of other.
   
<img src="https://i.imgur.com/VYaN9ny.png" height="80%" width="80%"/>

2. Change the permissions of the file identified in the previous step so that the owner type of other doesn’t have write permissions.

<img src="https://i.imgur.com/fEdjIMw.png" height="80%" width="80%"/>

3. The file project_m.txt is a restricted file and should not be readable or writable by the group or other; only the user should have these permissions on this file. List the contents and permissions of the current directory and check if the group has read or write permissions.

<img src="https://i.imgur.com/gyEiLwx.png" height="80%" width="80%"/>

4. Use the chmod command to change permissions of the project_m.txt file so that the group doesn’t have read or write permissions.

<img src="https://i.imgur.com/rurgwwV.png" height="80%" width="80%"/>

<h3>Task 3. Change file permissions on a hidden file</h3>

In this task, you must determine if a hidden file has incorrect permissions and then change the permissions as needed. This action will further remove unauthorized access and strengthen security on the system.

The file .project_x.txt is a hidden file that has been archived and should not be written to by anyone. (The user and group should still be able to read this file.)

1. Check the permissions of the hidden file .project_x.txt

<img src="https://i.imgur.com/CSbsY75.png" height="80%" width="80%"/>

2. Change the permissions of the file .project_x.txt so that both the user and the group can read, but not write to, the file.

<img src="https://i.imgur.com/HhngicJ.png" height="80%" width="80%"/>

<h3>Task 4. Change directory permissions</h3>

In this task, you must change the permissions of a directory. First, you’ll check the group permissions of the /home/researcher2/projects/drafts directory and then modify the permissions as required. (You should be in the projects directory while managing the permissions of its subdirectory drafts.)

Only the researcher2 user should be allowed to access the drafts directory and its contents. (This means that only researcher2 should have execute privileges.)

1. Check the permissions of the drafts directory.

<img src="https://i.imgur.com/DK2Hzc1.png" height="80%" width="80%"/>

2. Remove the execute permission for the group from the drafts directory.

<img src="https://i.imgur.com/hKYc9O9.png" height="80%" width="80%"/>



<h2>Conclusion</h2>

You now have practical experience in using basic Linux Bash shell commands to

- examine file and directory permissions
- change permissions on files
- change permissions on directories

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
