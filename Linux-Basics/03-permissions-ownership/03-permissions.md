# Linux file system permission
- Type of permission
  - Basic Permission
  - Special Permission
  - Access Control List
---
# For checking file permission
- ls -l /notes.txt
- output:
  - regular file: -rw-r-r-. 1 root root 0 jan 4 14:59 /notes.txt
<pre>
-rw-r-r- > permission
1 > link
root > owner
root > group owner
0 > size of file
jan 4 14:59 > date and time
/notes.txt > name of the file

</pre>

# For checking dir permission
- ls -ld /dev

# Permission in detail
* Permission classes:
 - user
 - group
 - other
---
# Types of files in Linux:

| Symbol | File Type         | Purpose                 |
| ------ | ----------------- | ----------------------- |
| `-`    | Regular File      | Data, scripts, binaries |
| `d`    | Directory         | Stores files            |
| `l`    | Symbolic Link     | Points to another file  |
| `c`    | Character Device  | Keyboard, mouse         |
| `b`    | Block Device      | Disk, storage           |
| `s`    | Socket            | IPC                     |
| `p`    | Named Pipe (FIFO) | Process communication   |

Example of usage:
* dir file:
drwxrwxrwx 2 user user mydir

* socket file:
srwxrwxrwx 1 root root /var/run/docker.sock
---
# Permission Group
Permission Description:
- Owner (u) →
 Permissions used for the owner of the file
- Group (g) →
 Permissions used by members of the group
- Other (o) →
 Permissions used by all other users

| Symbol | Meaning       | Value |
| ------ | ------------- | ----- |
| `r`    | Read          | 4     |
| `w`    | Write         | 2     |
| `x`    | Execute       | 1     |
| `-`    | No permission | 0     |

# Common permission Examples:
| Symbolic  | Numeric | Meaning                   |
| --------- | ------- | ------------------------- |
| rw------- | 600     | Private file              |
| rw-r--r-- | 644     | Public readable file      |
| rwxr-xr-x | 755     | Script / directory        |
| rwx------ | 700     | Owner only                |
| rwxrwxrwx | 777     | Full access (⚠ dangerous) |

---
# For change permission
* For add read permission to owner
- chmod u+r /notes.txt

* For add read write permission to group
- chmod g+rw /notes.txt

* For remove read permission to others
- chmod o-r /notes.txt
---
# For change ownership
- chown <user name> <file/directory name>
- ex: chown ajay /notes.txt

# For change group ownership

Syntax:
- chgrp <grp name> <file/dir name>
- ex: chgrp devops /notes.txt
---
# Linux permissions are written as:
<pre> [ special ][ owner ][ group ][ others ]</pre>
# Valid ranges
⦁	Special bit → 0–7
⦁	Owner → 0–7
⦁	Group → 0–7
⦁	Others → 0–7

| Permission | Special Bit | Name           | Applies To          | Meaning                                                                            |
| ---------- | ----------- | -------------- | ------------------- | ---------------------------------------------------------------------------------- |
| **4755**   | 4           | **setuid**     | Files               | Runs with **owner’s (root) privilege**                                             |
| **2755**   | 2           | **setgid**     | Files / Directories | Files: run with **group privilege**<br>Dirs: new files inherit **group ownership** |
| **1755**   | 1           | **Sticky bit** | Directories         | Only **file owner or root** can delete files                                       |



# Set permission with a numeric value
- For set permission with a numeric value
  - r (read) = 4
  - w (write) = 2
  - x (execute) = 1
- ex: chmod 751 /ramu
---
# Access Control List

⦁	Access control list (ACL) provides an additional, more flexible permission
mechanism for file systems.
⦁	Access control list is a service which is used for providing special permission
to specific users and group to particular directories and file
Use of ACL

<pre> Think of a scenario in which a particular user is not a member of group created
by you but still you want to give some read or write access, how can you do it
without making user a member of group, here comes in picture Access Control
Lists, ACL helps us to do this trick.</pre>

* For check ACL permission:
  - getfacl <file / dir>
* For set ACL permission to user:
  - 'setfacl -m u:ramu:rwx /dev'
* remove ACL:
  - 'setfacl -x u:ramu: /dev'
* For set ACL permission to group:
  - 'setfacl -m g:devops:rwx /dev'
* For remove all ACL permissions:
  - 'setfacl -b /dev'
