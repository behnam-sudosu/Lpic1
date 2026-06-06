# cron and at  

### ANACRON

```bash
#for desktop
anacron
```

---

### cron

 	vim /etc/crontab

```bash
# you can edit and set
minutes - hour - day of month - month - day of week - name user - command or direction
	*        *          *          *          *           root        shutdown -P
	*        *          *          *          *           root        /home/behnam/ping.sh
*/1
*/2
#and
#15,22,56 defrence minutes
,

#until
#15-26 between 15-26
-

#when server reboot do something
@reboot

#do daily
@daily

#do weekly
@weekly

#do monthly
@monthly

#do yearly
@yearly
```
```bash
#for desktop linux and only root can make cron
unacron

#set cron for user
crontab -e

#these are vise versa and if server reboot the cron dosn't excute but anacron excute
cron and anacron

#first you have to write script then put it in cron
script

#you can set daily but not important when
/etc/cron.d

/etc/cron.daly

/etc/cron.d

/etc/cron.hourly

/etc/cron.mounthly

/etc/cron.weekly

#show log cron job
cat /var/log/syslog | grep -i cron
```

---  

### at  

```bash
#use only one time
at

apt install at

at 5:45
	ls
	cd /tmp
	ctrl + d

at 10:00 am Mon
at 10:00 am July 27
at 10:00 am 2024
at 10:00 am 08/22/225
at 10:00 am next mounth
at 10:00 am tomorrow
at now + 1 week
at now + 1 hour
at now + 1 mounth
at now + 1 year

#for run your script
at
	bash /tmp/ping.sh

#4 o'clock
at teatime

#12 o'clock
at midnight

#show all at you set
atq

#remove at
atrm 
```

---  

### add user cron and at

 ```bash
/etc/cron.allow ===>> allow user to make cron
/etc/cron.deny ===>> deny user to make cron
/etc/at.allow ===>> allow user to make at
/etc/at.deny ===>> allow user to make at
```
```bash
#who can make cron
vim /etc/cron.allow
	milad
	behnam  
```

---  

### when you take server for the first time check this  

```bash
atq
cron
/etc/crontab
/etc/cron.d
/etc/cron monthly or yearly
```