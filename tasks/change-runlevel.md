# change runlevel  

### vim /etc/default/grub
```bash
GRUB_DEFAULT=0
GRUB_TIMEOUT_STYLE=hidden
GRUB_TIMEOUT=10
GRUB_DISTRIBUTOR=`lsb_release -i -s 2> /dev/null || echo Debian`
GRUB_CMDLINE_LINUX_DEFAULT="" 
#put number between "", the number must be between 0 and 6
GRUB_CMDLINE_LINUX=""
#never use 0 because if use 0 before come os up is go to the hal
#nver use 0 because if use 6 after come up os reboot system again and again
```
```bash
save the file
```
---  

### commands

```bash
#the number must be between 1 and 6
systemctl set-default (number of runlevel)

#show run level
runlevel

#change runlevel
init NUMBER
```