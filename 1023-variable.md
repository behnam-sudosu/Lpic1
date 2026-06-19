# make variable

```bash
VAR1=behnam
echo $VAR1
echo my name is $VAR1
echo my name is ${VAR1}
echo my name is ${VAR1}emami
export ===>> show all environment variable
export VAR1 ===>> you can have in all shell
env ===>> show all environment variable
set ===>> change behaviar shell
set -u ===>> show unknow
set +u ===>> don't show unknow
unset VAR1 ===>> delete variables
export VAR1 ===>> you can use every shell
echo $$ ===>> show uuid
exit
```
```bash
save the file
export ===>> show all environment variable
env ===>> show all environment variable
```

---

### environment variables

```bash
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
```

---

### directory

```bash
export LD_LIBRARY_PATH = /home/behnam/lib
export LD_LIBRARY_PATH = /home/behnam/lib:/home/behnam/develop/udevlib/out
export LD_LIBRARY_PATH = /home/behnam/lib:/home/behnam/develop/udevlib/out:/opt/externalsoftware/lib
```