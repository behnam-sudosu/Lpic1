## System info

	date ===>> Show the current date and time
	date +%s ===>> show more about time
	date -u ===>> UTC time

	cat /proc/cpuinfo ===>> show cpu information
	cat /proc/meminfo ===>> show memory information
	cat /proc/filesystem ===>> show all file system linux
	cat /proc/uptime
	cat /proc/monts ===>> show all mounts point

	/proc ===>> kernel configurtain
	/sys ===>> hal configurtion

	cat /sys ===>> same as proc

	lscpu ===>> more information about cpu
	lsusb ===>> more information about usb
	lshw ===>> information about all your hardware
	lsmem ===>> more information about memory
	lspci ===>> more information about your connectore


	lsmod ===>> show all modules
	-v ===>> verbose more information
	lsmod
	rmmod NMAE_MODULES
	instmod NMAE_MODULES
	modeprobe -r NAME_MODULES ===>> remove modules
	modeprobe NAME_MODULES ===>> start modules

	#location of installed and available modules
	cd /lib/modules

	#creates and updates modules.dep
	depmod

	#upgrade
	depmod -a

	#information about a module
	modinfo NAME_MODULES

	enable ===>> install
	disable ===>> uninstall
	remove ===>> after restart come up
	cat /proc/modules ===>> show all modules
	cat /etc/modules ===>> modules configuration
	cat /etc/modprobe.d ===>> modules configuration

	blkid ===>> show uuid
	lsblk ===>> show all disk
	
	
	

	man command ===>> Show the manual for command
	df ===>> Show the disk usage
	du ===>> Show directory space usage

	

	wc -l (name of file) ===>> show how many lines have the file

	dmesg ===>> show logs when the os is up
	cat /var/log/syslog ===>> show all logs

	lsb_release -a ===>> show your os
	cat /etc/os-release ===>> show your os
	

	top ===>> show cpu and memory and network usage
	pgrep (name program) ===>> find process id

	which ls
 	whereis ls
	whereis app ===>> Show possible location of app
	which app ===>> Show which application will be run by default
	file ===>> show your type of file
	uptime ===>> Show current uptime
	w ===>> Display who is on line
	whoami ===>> Who you are logged in as
