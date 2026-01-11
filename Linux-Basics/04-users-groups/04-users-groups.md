# User Management
- useradd deva -> create user
- passwd devuser -> create user password
- grep ramu /etc/shadow -> user password properties
- su rakesh -> switch user
- userdel ramu -> delete user
- usermod -l shiva ramu -> change user login name

# Group Management
- groupadd devops -> add group account
- grep devops /etc/group -> group properties
- grep devops /etc/gshadow -> check group admin properties
- groupdel devops
- gpasswd -a ajay devops -> add single member in group
- gpasswd -M Rahul, Ramesh, Rakesh, devops -> add multiple members in group
- gpasswd -d Ramesh devops -> remove group member
- gpasswd -A rakesh devops -> make group admin

# 👤 useradd
-m → create home directory
-d → custom home directory
-s → login shell
-u → user ID
-g → primary group
-G → secondary groups
-c → user comment
-e → account expiry
-r → system user

# 👤 usermod
-a → append group
-G → add secondary group
-g → change primary group
-d → change home directory
-s → change shell
-l → rename user
-L → lock user
-U → unlock user
-e → change expiry

# 👤 userdel
-r → delete home directory

# 🔐 passwd
-l → lock password
-u → unlock password
-d → delete password
-e → expire password

# 👥 groupadd
-g → group ID
-r → system group

# 👥 groupmod
-g → change group ID
-n → rename group

# 👥 gpasswd
-a → add user to group
-d → remove user
-A → group admin
-M → group members

# 🔍 id
-u → show UID
-g → show GID
-G → show groups
  
# Important files:
- /etc/passwd
- /etc/shadow
- /etc/group
