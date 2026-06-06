# new debian
	copy grub
	change to root
	sudo apt update
	apt install sudo
	sudo apt install vim
	sudo apt install net-tools
	sudo apt install tmux, byobu
	sudo apt install tree
	change user as sudoer
		sudo visudo ===>> username ALL=(ALL:ALL) ALL
		sudo usermod -aG sudo debian
	check bash_login
	check bash_logout
	check .bashrc
	check at 
	check cron
	check aliases
	check systemd
	mkdir ~/.ssh
	touch authorized_keys
	or ssh-keygen -t RSA	
	alias ===>> ll, poweroff, reboot, shutdown -p
	scp -P4000 .bash_aliases debian@192.168.1.105:/home/debian
	

	vim /etc/network/interfaces
	allow-hotplug ens36
	# The loopback network interface auto lo iface lo inet loopback
	# The primary network interface
	auto ens36
	iface ens36  inet static
		address 192.168.2.236
		netmask 255.255.255.0
		gateway 192.168.2.254
		dns-nameservers 192.168.2.254
	 
	sudo systemctl restart networking.service
	sudo vim /etc/resolv.conf
		nameserver 8.8.8.8
		nameserver 4.2.2.4
	 
	sudo apt install ntp ===>> git-hub/tasks/lpic1/NTP-server
		vim /etc/ntp.conf
	nfs ===>> git-hub/tasks/Devops/nfs
	Banner login ===>> git-hub/tasks/lpic2/notifaction
	fdisk ===>> git-hub/tasks/lpic2/fdisk&make-swap
	lvm ===>> git-hub/tasks/lpic2/lvm or git-hub/tasks/Devops/lvm
	swap ===>> git-hub/tasks/lpic2/fdisk&make-swap
	aliases
	raid ===>> git-hub/tasks/lpic2/raid
	
# set two interfaces
	#allow-hotplug enp1s0
	auto enp1s0
	iface enp1s0 inet static
		address 192.168.1.125
		netmask 255.255.255.0
		gateway 192.168.1.1
		dns-nameservers 8.8.8.8
	iface enp1s0 inet static
		address 192.168.1.127
		netmask 255.255.255.0
	
	#allow-hotplug enp9s0
	auto enp9s0
	iface enp9s0 inet static
		address 192.168.1.129
		netmask 255.255.255.0
	iface enp9s0 inet static
		address 192.168.1.130
		netmask 255.255.255.0
	

# secure

	find / -perm -u+s > suid8.txt ===>> -u = user
	find / -perm -g+s > suid8.txt ===>> -g = group
	find / -perm -u+s > suid7.txt ===>> after six mounth
	find / -perm -g+s > suid8.txt ===>> after six mounth
	diff suid7.txt suid8.txt

	copy superblock

	sudo apt install cdpr ===>> network which port you connect and interface