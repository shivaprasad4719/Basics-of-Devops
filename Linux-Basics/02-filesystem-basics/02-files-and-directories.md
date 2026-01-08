# Linux File System Structure
* **/** – Root directory
* **/home** – User home directories
* **/etc** – Configuration files (" It controls the behavior of an operating system or application")
* **/var** – Logs & variable data
  - /var/lib: Contains database and package files.
  - /var/mail: Contains Emails.
  - /var/tmp: Contains Temporary files needed for reboot

* **/usr** – User binaries & programs
* **/mnt** - Mount Directory ("used to mount a file system temporarily.")
* **/dev** → Device Files
* **/bin** → User Binaries ("Contains binary executable."
---

# Common Commands
- **pwd** → it shows the present working directory
- **ls** → it shows available files and directory list in the present working directory.
- **uname** → it shows the name of the kernel (OS)
- **uname -r** → it shows version of the kernel
- **cd** → it use for change directory
- **clear** → it use for clear screen
- **whoami** → it show currently login user name
- **history** → it show list of previously used commands
- **date** → it show time and date
- **rm** → Remove files or directories

---

# Create directory

- **mkdir /bird** - single directory
- **mkdir bird animal human** - multiple directories
- **mkdir -p /bird/parrot** - create dir path (inside dir)
- **mkdir /students{1..10}** - create number of dir (two dots)

---

# Create file

- **touch notes.txt** - single file of any format
- **touch notes.txt web.html animals** - multiple files
- **touch books{1..10}** - create number of files (two dots)

---


# For copy and paste
**cp** : cp command is used for copy and paste file or directory
Syntax:
- **cp <option> <source> <destination>**
# Options:
* **-r** for recursive (Not needed for a single file, but doesn’t cause an error)
* **-v** for verbose (Helpful for confirmation & logs)
* **-f** for forcefull (Overwrites existing files without asking **Be careful: data loss possible**)

# Example commands:

- **cp -rvf /root/birds.txt /home**
In this example we used 3 options

- **cp -rvf /root/D\* /home**
Here, copying all data that start form D alphabet

# For move or rename file & directory:
1. For move file or directory
- **mv /home/parrot /root/birds**
Here the file/dir is moving to the destination dir birds.

2. For rename file or directory

- **mv tree birds**
Here tree replacing the birds.

