# Linux Commands

### ls

```bash
ls --help ===>> show all help
ls ===>> Directory listing
ls -1 ===>> show vertical
ls -a ===>> Formatted listing with hidden files
ls -l ===>> long detail listing
ls -lt ===>> Sorting the formatted listing by time modification
ls -R ===>> recursive view
ls -r ===>> reverse
ls /dev | grep sda ===>> show only sda in ls
ls ? ===>> ?=ls one character
ls ?? ===>> two character
ls * ===>> any character
ls [a-zA-Z0-9]
ls [a-c]*
ls *.txt
ls 1*.txt
ls 1?.txt
ls f* ===>> only start with f
ls ! ===>> bar reverse
```

---

### cat commands

```bash
cat file ===>> show file text
cat -n file ===>> show number
cat > file3 ===>> write in this file
	ctrl + d ===>> go out side the file
ls -l /chert 2>&1 > file1
cat -n ===>> show enter
nl ===>> dosn't show enter
cat file1 | grep -i any | wc -l
diff fiel1 file2 ===>> show diffrence of two files
tac FILE_NAME ===>> show in end file
```

---

### cd

```bash
cd dir ===>> Change directory to dir
cd ===>> Change to home directory
cd .. ===>> back to last directory
cd - ===>> back to last directory you had been
cd ===>> back to home directory
cd ~ ===>> back to home directory
cd ===>> exact path, partially path
. ===>> curent directory
.. ===>> above directory
```

---

### cut

```bash
cut ===>> shows special column or field
cut -c3-5 FILE_NAME ===>> third to fifth
cut -c3,5 FILE_NAME ===>> 
cut -c3- FILE_NAME ===>> after third
cut FILE_NAME -d"-" -f2 ===>> culume two
cut FILE_NAME -d: -f2 ===>> culume two
cut -d"-" -f2-4
cut -f2 -d " " ( in doble cot has space)
```

---

### path

```bash
echo $PATH ===>> show path directorys
PATH=PATH:/direction
.bashrc ===>> peranent
export PATH="direction":$PATH
```

---

### tee

```bash
tee ===>> show excute (like >)
tee -a ===>> append (like >>)
tee ===>> copy file and directory but show everything
tee ===>> show on scren
```

---

### tr commands

```bash
tr is IS
tr [:lower:] [:upper:]
tr [:space:] '\t' ===>> use tab
tr -d [:digit:] ===>> clean digit
tr -dc [:digit:] ===>> clean word
```

---

### cp

```bash
cp ===>> copy files and folders
cp file1 file2 ===>> Copy the contents of file1 ro file2
cp -r dir1 dir2 ===>> Copy dir1 to dir2;create dir2 if not present
cp -R dir1 dir2 ===>> Copy dir1 to dir2;create dir2 if not present
cp -i ===>> first ask it
cp -b ===>> take backup (~)
```

---

### scp

```bash
scp ===>> copy file or directory
scp mydir.tar behnam@192.168.1.100:/tmp
scp behnam@192.168.1.100:/tmp/mydir.tar .
scp -r mydir behnam@192.168.1.100:/tmp ===>> directory
```

---

### splite

```bash
truncat ===>> splite
split -l 3 file1 ===>> seprate file in line
splite -b 1000MB file1 ===>> seprate file in weght
splite -l5 (name file) ===>> (-l = seprate kine)
splite b40 (name file) ===>> (b = bite)
splite b40 -d (name file) ===>> -d = digit number
splite b40 output ===>> make name output
cat out* > file name ===>> assenble file that you splite
```

---

### wc

```bash
wc ===>> word count, count's number of lines, words and character
wc -l ===>> show line
wc -w ===>> show word
wc -c ===>> show character
wc * ===>> show all file in this directory
```

---

### history

```bash
history ===>> show all command you used
history 20 ===>> show only 20 command you used
history -c ===>> clean
```

---

### du & df

```bash
du ===>> disk usage, show size file
# s = show size of file in this directory
du -sh

# * show all file size
du -sh *

du -sha
# h = human readable
du -h

df ===>> disk free

# h = human readable
df -h
df -h /

# T = type file system
df -hT
df -i ===>> inod
```

---

### head & tail

```bash
head FILE_NAME ===>> viewing beginning of a file
head -n 20 ===>> show 20 lines
tail FILE_NAME ===>> viewing end of a file
tail -n 20 ===>> show 20 line
tail -20 ===>> show 20 line
tail -f file ===>> Output the contents of file as it grows,starting with the last 10 lines
tail -f /var/log/syslog ===>> this is good for log
more file ===>> Output the contents of the file
less file ===>> open files for viewing, scroll, good for large files and read zip files
```

---

### touch

```bash
touch file ===>> create empty file or update last access time, file with name and no content
touch file{1..100}.txt ===>> you can make 10 file
touch -t 2025-12-24-16:57 FILE_NAME
accesstime ===>> atime ===>> a
modifytime ===>> mtime ===>> c
changetime ===>> ctime ===>> m

touch -r filename filename===>> change time
touch file_backup_$(date +%Y%m%d).log ===>> touch file with calender
```

---

### mv

```bash
mv ===>> move files and directorys and change name
mv -r ===>> this is for folder
```

---

### rm

```bash
rm ===>> by default only removes files but can also remove directory
rm file ===>> Deleting the file
rm -r dir ===>> Deleting the directory
rm -f file ===>> Force to remove the file
rm -rf dir ===>> Force to remove the directory dir
rmdir ===>> removes empty directories
```

---

### mkdir

```bash
mkdir dir ===>> Creates directories
mkdir -p ===>> make parents directories
```

---

### search & exit

```bash
!vim ===>> excute last file with vim
!cat ===>> execute last command with cat
!! sudo ===>> execute last command in sudo
!! ===>> execute last command
!?vim? ===>> excute last command vim
ctrl + R ===>> search in command
	r ===>> go back command
exit ===>> Logout the current session
logout ===>> Logout the current session
ctrl + d ===>> Logout the current session
```

---

### nl

```bash
nl ===>> number line
nl -nln ===>> left to right
nl -nrn ===>> right to left
nl -nrz ===>> put zero befor number
nl ===>> dosn't show enter
```

---

### Commands

```bash
paste ===>> open two file for moghayese
paste file1 file2 ===>> merge two file
paste -d: file1 file2 ===>> merge two file with
pwd ===>> show current working directory
top ===>> Display all running process
id NAME ===>> shows information about the users
id behnam ===>> more information
passwd ===>> reser password
join ===>> good for script database
join FILE_NAME FILENAME
whereis passwd
which ping
type ping ===>> show directory
which ls
whatis ls
file FILE_NAME ===>> show type of file
file -i name-file
uptime ===>> Show current uptime
w ===>> what logged in user are doing
stat ===>> show time change
stat file1 ===>> show all
uuid ===>> universal uniq ID
uuidgen ===>> make a new uuid
wall ===>> send massage to other user
ctrl + alt + f1 ===>> real terminal in linux
sudo apt install mplayer
mplayer ===>> play music in terminal
mplayer PATH
open ssl rand
tc ===>> traffic control
CDN ===>> countaint delevery network
snmp ===>> port for monitoring
elinks (URL) ===>> open browser in terminal
~ ===>> home directory
$ ===>> user
# ===>> root
hal ===>> hardware abstraction layer
udev ===>> set rule
; ===>> excute all cammand
|| ===>> or
0 1 ===>> 1
1 0 ===>> 1
1 1 ===>> 1
0 0 ===>> 0
&& ===>> and
0 1 ===>> 0
1 0 ===>> 0
1 1 ===>> 1
0 0 ===>> 0
echo $? ===>> 0=means correct, 1=means incorect
auditd = log
var/log/wtmp ===>> how type reboot
nfs ===>> network file system
sudo bash ===>> root login
cat /etc/group
cat /etc/passwd
lsblk ===>> show all disk and partition
blkid ===>> uuid disk
cat -n ===>> show enter
su USER_NAME ===>> change user
su ===>> change user to root
sudo su - ===>> login user root
whoami
who ===>> who is logged in
ls --help ===>> information about ls
man ls ===>> more information about ls
apropos = man
apropos ls
info ls ===>> less information
> ===>> direct
>> ===>> append
ntp ===>> network protocol utc
pr ===>> print
fmt -w 3- fiel1 ===>> show in old monitor
yes > file1 ===>> make file
sudo apt install tree
tree dir1 ===>> show everything in direcrory
fnt -w 15 FILE_NAME ===>> show in small page
awk ===>> language program
HAL ===>> hardware abstraction layer
UDEV ===>> rules and events
DBUS ===>> communicate with each other
hot blug
cold plug
clear ===>> clean the scren
exec ls ===>> take ls and then close shel
/var/log/dmesg ===>> show kernel ring buffer (kernel only)
/var/log/syslog ===>> show all
```