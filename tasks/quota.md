# quata

### quata help you for limit user have storage

```bash
apt install quota
```
```bash
quotaoff -a
vim /etc/fstab
    defaults
    usrquota
    grpquota
```
```bash
umount /de/sdb1
mount /dev/sdb1
```
```bash
~/quata
quotacheck -cug /dev/sdb1
    -c ===>> create
    -u ===>> user
    -g ===>> group
```
```bash
edquota -U behnam
    blocks   soft   hard   inodes   soft   hard
        kb      70m    100m    
quotaon -a
```
```bash
quota /dev/sdb1
edquota -t ===>> change day expire
repquota -a ===>> report
repquota /dev/sdb1
```