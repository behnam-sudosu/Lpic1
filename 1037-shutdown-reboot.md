## shutdown & reboot  

	shutdown
	shutdown -P ===>> poweroff
	shutdown -h ===>> halt
	shutdown -r ===>> reboot
	shutdown -r now ===>> reboot
	shutdown -c ===>> cancel
	shutdown -r now
	shutdown -r 2 going down after 2 min ===>> send wall automaticly
	shutdown -r 13:15 
	shutdown -P +15
	shutdown -t ===>> 60 sec before kill all program
	reboot -p ===>> poweroff
	reboot -f ===>> force
	poweroff -P ===>> shutdown
	poweroff -f ===>> force
	/var/log/wtmp ===>> show who reboot the server
	halt -p
	halt -f
	telinit 6
	init
