# runlevel

```bash
 runlevel  		|				debian			   |		redhat  
------------------------------------------------------------------------------------------
	0			|				halt			   |  		halt
------------------------------------------------------------------------------------------
	1 			|	    	    single user	       | 		single user
------------------------------------------------------------------------------------------
	2			|	   		    multi user, gui    |  		multi user, without GUI
------------------------------------------------------------------------------------------
	3			|	   		    full multi user    | 		multiuser without network
------------------------------------------------------------------------------------------
	4   		|             	nothing            |        nothing
------------------------------------------------------------------------------------------
	5   		|               full multi user	   |        multi user, with GUI
------------------------------------------------------------------------------------------
	6   		|          	    reboot             |        reboot
```

---

### change runlevel

```bash
runlevel ===>> show your curent runlevel
telinit 3 ===>> change runlevel
init 5 ===>> change runlevel
```

---

### change and edit grub directory

```bash
/etc/default/grub
/etc/grub.d
/boot/grub/grub.conf
```

---

### script of service

```bash
# you can stop, start, reload, status service
/etc/init.d/lvm start
./lvm start

# old os
/etc/inittab
```

---

### set runlevel

```bash
etc/init.d
	s ===>> start
	k ===>> kill
```

---

### set runlevel with link

```bash
etc/rc
```

---

### commands

```bash
# for systemd
systemctl
systemctl list ===>> show all list service
systemctl start ssh

# for upstart
initctl
/etc/init ===>> config file

# old cammand
service sendmail stop

# show all start and kill service
chkconfig --list ===>> centos
service --status-all ===>> debian

# install on debian
apt install chkconfig
chkconfig SERVICE_NAME on
chkconfig SERVICE_NAME off

# reload all service
systemctl daemon-reload
```

---

### save systemd file directory

```bash
# script of service
/etc/init.d

# first direction save systemd
/etc/systemd/system  
	# name service with .service
	file.service

# second directory save systemd
/usr/lib/systemd/system
	#name service with .service
	file.service

# for login user
/etc/profile.d
	# name service with .sh
```