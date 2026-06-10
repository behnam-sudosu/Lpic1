# new ubuntu
	copy grub
	sudo apt update
	sudo apt install vim (if minimal os)
	sudo apt install iputils-ping
	sudo apt install net-tools ===>> ifconfig
	sudo apt install tmux, byobu
	sudo apt install tree
	hostnamectl set-hostname srv2
	vim /etc/hosts
	vim /etc/hostname
	check bash_login
	check bash_logout
	check .bashrc
	check at 
	check cron
	check aliases
	check systemd
	change /etc/apt/sources.list to us and ir
	change password root
	copy publickey to server
	change ip /etc/netplan/*.yamel
		network:
		  version: 2
		  renderer: networkd
		  ethernets:
		    ens3:
		      dhcp4: no
		      addresses:
				- 192.168.121.221/24
				gateway4: 192.168.121.1
				nameservers:
				addresses: [8.8.8.8, 1.1.1.1]
			  
		netplan try or netplan apply
		
		sudo vim /etc/ssh/sshd_config
			config file	
	unlink /etc/resolv.conf
	vim /etc/resolv.conf
		nameservers 8.8.8.8
		nameservers 4.2.2.4
	set interface
	set ip
	touch /home/behnam/.ssh/config
		include /home/behnam/.ssh/config.d/*.conf
	config /home/behnam/.ssh/config.d
		Host srv1
			HostName 192.168.1.110
			Port 22
			User behnam
			BindAddress 192.168.2.100

	scp -P4000 .bash_aliases ubuntu@192.168.1.115:/home/ubuntu
	
	sudo apt install ntp ===>> git-hub/tasks/lpic1/NTP-server
		vim /etc/ntp.conf
	nfs ===>> git-hub/tasks/Devops/nfs
	Banner login ===>> git-hub/tasks/lpic2/notifaction
	fdisk ===>> git-hub/tasks/lpic2/fdisk&make-swap
	lvm ===>> git-hub/tasks/lpic2/lvm or git-hub/tasks/Devops/lvm
	swap ===>> git-hub/tasks/lpic2/fdisk&make-swap
	aliases
	raid ===>> git-hub/tasks/lpic2/raid

	
			
			
	
# secure

find / -perm -u+s > suid8.txt ===>> -u = user
find / -perm -g+s > suid8.txt ===>> -g = group
find / -perm -u+s > suid7.txt ===>> after six mounth
find / -perm -g+s > suid8.txt ===>> after six mounth
diff suid7.txt suid8.txt
	
	copy superblock
	
	sudo apt install cdpr ===>> network which port you connect and interface
