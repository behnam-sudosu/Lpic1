# permision on file and directory 

### permision

```bash
informastion

d ===>> directory
- ===>> file
l ===>> link
```
```bash
permission

r ===>> read
w ===>> write
x ===>> excute

chmod ===>> change permision
chown ===>> change owner and group
chgrp ===>> change group
```
```bash
#u = user
chmod u+w file1

#take w from
chmod u-w file1

#g = group
chmod g+wx file1

#o = others
chmod o+rwx file1

chmod u+rwx,g-rx,o-r file1

#a=all
chmod a=wx file1

#all
chmod all=rwx

#all file in folder
chmod -r or -R
```

```bash
touch file{1..10}.txt

#-R = parents
chmod -R 777 dir1

#where is passwd command
which passwd

			r	w	x
permision	4	2	1  
```

---  

### second permison  

```bash
suid ===>> for user
guid ===>> for group
sticky bit ===>> for owner

chmod 4644 file1
			r	w	x
permision	4	2	1
4 ===>> suid
2 ===>> guid
1 ===>> sticky bit

	s ===>> have x
	S ===>> dont have x
umask ===>> give all permision  
```

---  

### group and owner change  

```bash
chown behnam:root file1
chown behnam: file1

#all file in directory change to root owner
chown root FILE_NAME -R

chgroup milad file1

#you can find passwd
which passwd

#show all users
cat /etc/passwd

#show all groups
cat /etc/group
```

---  

### secure server

```bash
#-u = user
find / -perm -u+s > suid8.txt

#-g = group
find / -perm -g+s > suid8.txt

#make dif
	find / -perm -u+s > suid7.txt

	#after six mounth
	find / -perm -g+s > suid8.txt
	
	#find file why change permission
	diff suid7.txt suid8.txt
```

---  

# sodoer  

```bash
/etc/sudoers.d
    behnam ALL=(ALL) NOPASSWD:ALL
```