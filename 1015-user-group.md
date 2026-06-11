# users

```bash
id USER_NAME ===>> say id and uid and group id
last ===>> shows recently logins (auditing)
passwd USER_NAME ===>> changing user passwords
passwd ===>> change curent user
cat /etc/passwd ===>> show all users
cat /etc/group ===>> show all groups
cat /etc/shadow ===>> save password here
hint: id and user if have 0 can do everything
```

---

### change hostname

```bash
# change hostname
/etc/hosts
/etc/hostname
hostnamectl set-hostname USER_NAME
```

---

### add user

```bash
# adding user in linux
useradd or adduser USER_NAME

# make home directory
adduser -m

# change home directory
adduser -d

# make command
adduser -c "admin server" NAME_USER

# change shell (sh is current)
adduser -s "/bin/bash"
useradd -m ===>> home
useradd -c ===>> "command"
useradd -d ===>> home direction
useradd -s ===>> "/bin/bash"
```
```bash
# show users
cat /etc/passwd

# only show USER_NAME
cat /etc/passwd | grep -i USER_NAME
```

---

### modified user

```bash
# modifying user properties
usermod

# set comment
usermod -c "admin" USER_NAME

# set bash for user
usermod -s "/bin.bash"

# change home directory
usermod -d

# lock the user
usermod -L USER_NAME

# unlock user (after that reset password)
usermod -U USER_NAME

# change primary group
usermod -g adm USER_NAME

# join another groups
usermod -G sudo USER_NAME

# join user to group sudoers nad append
usermod -aG sudo USR_NAME
```

---

### delete user

```bash
# deleting a user
userdel USER_NAME

# remove home directory and mail spool
userdel -r USER_NAME

# force removal of files, even if not owned by user
userdel -f USER_NAME
```

---

### groups

```bash
cat /etc/group

# adding groups to linux
groupadd USER_GROUP

# change id and name group
group -g 1005

# set pass on group
gpasswd

# deleting a user
groupdel
```

---

### modify group

```bash
# change name group1
groupmod -n newgroup NAME_GROUP

# change id
groupmod -g 1010 newgroup
```

---

### delete group

```bash
# delete group
groupdel NAME_GROUP
```

---

### privilage

```bash
cat /etc/sudoers

# make file name your user
cat /etc/sudoers.d/
	# no need password for login to root
	USER_NAME ALL=(ALLNOPASSD:ALL)
```

---

### more information about user

```bash
# show information behnam and last modify
chage -l USER_NAME
chage USER_NAME

# like a grep in file passwd
getent passwd USER_NAME
```

---

### add user

```bash
# change name
sudo usermod -l NEW_USER OLD_USER

# change group
sudo groupmod -n NEW_USER OLD_USER

# change home directory
sudo usermod -d /home/NEW_USER -m NEW_USER
```