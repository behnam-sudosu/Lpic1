# ldd
	ldd ===>> show your shared library

### file library save here
	/lib
	/lib64
	/usr/lib
	/usr/lib64
	/usr/local/lib

### find path command
	which ls
		/usr/bin/ls
	whereis sudo
		/usr/sbin/sudo
	type ls
		/usr/bin/ls
	echo $PATH ===>> show your all path
 	
### find library command
	ldconfig ===>> cash your shared library
	ldd /usr/bin/ls ===>> share library

### directory for ldd
 	cat /etc/ld.so.conf ===>> config file
 	/etc/ld.so.conf.d/*.conf
		/usr/local/lib
		/lib
		/usr/lib
 	cat /etc/ld.so.cash ===>> show cash your shared library

### environment variable
	export ===>> show all environment variable
	env ===>> show all environment variable

	export LD_LIBRARY_PATH = /home/behnam/lib
	export LD_LIBRARY_PATH = /home/behnam/lib:/home/behnam/develop/udevlib/out
	export LD_LIBRARY_PATH = /home/behnam/lib:/home/behnam/develop/udevlib/out:/opt/externalsoftware/lib

	echo $USER ===>> the name of the logged-in user
	echo $UID ===>> the numeric user id of the logged-in user
	echo $HOME ===>> the user's home directory
	echo $PWD ===>> the current working directory
	echo $SHELL ===>> the name of the shell
	echo $$ ===>> the process id running bash shell
	echo $PPID ===>> the process id of the process that started this process
	echo $PATH ===>> show path directorys
	echo $HISTFILE ===>> save history
	echo $HISTsize ===>> save size of history
	echo $? ===>> the exit code of the last command
		0 ===>> right
		1 ===>> wrong