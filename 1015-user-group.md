# users  

```bash
id NAME_USER ===>> say id and uid and group id
last ===>> shows recently logins (auditing)
passwd behnam ===>> changing user passwords
passwd ===>> change curent user
cat /etc/passwd ===>> show all users
cat /etc/group ===>> show all groups
cat /etc/shadow ===>> save password here
hint: id and user if have 0 can do everything  
```

---  

### change hostname

```bash
#change hostname
/etc/hosts
/etc/hostname 
hostnamectl set-hostname NAME
```
### add user

```bash
#adding user in linux
useradd or adduser NAME-USER

#make home directory
adduser -m

#change home directory
adduser -d

#make command
adduser -c "admin server" NAME_USER

#change shell (sh is current)
adduser -s "/bin/bash"
useradd -m ===>> home
useradd -c ===>> "command"
useradd -d ===>> home direction
useradd -s ===>> "/bin/bash"
```
```bash
#show users
cat /etc/passwd

#only show behnam 
cat /etc/passwd | grep -i NMAE_USER
```

---  

### modified user  

```bash
# modifying user properties
usermod

#set comment
usermod -c "admin" NAME_USER

#set bash for user
usermod -s "/bin.bash"

#change home directory
usermod -d

#lock the user
usermod -L NAME_USER

#unlock user (after that reset password)
usermod -U NAME_USER

#change primary group
usermod -g adm NAME_USER

#join another groups
usermod -G sudo NMAE_USER

#join user to group sudoers nad append
usermod -aG sudo NAME_USER
```

---  

### delete user  

```bash
#deleting a user
userdel NAME_USER

#remove home directory and mail spool
userdel -r NAME_USER

#force removal of files, even if not owned by user
userdel -f NAME_USER
```

---  

### groups  

```bash
cat /etc/group

#adding groups to linux
groupadd soc

#change id and name group
group -g 1005

#set pass on group
gpasswd

#deleting a user
groupdel
```

---  

### modify group  

```bash
#change name group1
groupmod -n newgroup group1

#change id
groupmod -g 1010 newgroup 
```

---  


### delete group  

```bash
#delete group
groupdel group1
```

---  

### privilage

```bash
cat /etc/sudoers

#make file name your user
cat /etc/sudoers.d/
	#no need password for login to root
	NAME_USER ALL=(ALLNOPASSD:ALL)
```

---  


### more information about user  

```bash
#show information behnam and last modify
chage -l NAME_USER
chage NAME_USER 

#like a grep in file passwd
getent passwd NAME_USER
```

### wrong add user

```bash
# change name
sudo usermod -l NEW_USER OLD_USER

# change group
sudo groupmod -n NEW_USER OLD_USER

# change hoem directory
sudo usermod -d /home/NEW_USER -m NEW_USER
```