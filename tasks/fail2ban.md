# fail2ban

### install fail2ban

```bash
sudo apt update && sudo apt install fail2ban
```
---

### enable service

```bash
cd /etc/fail2ban
cd /etc/fail2ban/filter.d ===>> config file all application
```
```bash
# check service is active
systemctl status fail2ban.service

# enable service
systemctl enabled fail2ban.service
```

---

### make new file

```bash
touch /etc/fail2ban/jail.local
vim /etc/fail2ban/jail.local
```
```bash
[sshd]
enabled = true
banaction = iptables-multiport
maxretry = 10
findtime = 43200
bantime = 86400
```
```bash
cd /etc/fail2ban
jail.conf
    [sshd]
    enabled = true
    [INCLUDEs]
    [DEFAULT]
    gnorep=127.0.0.1
    bantime = 15 seconds
    findtime = 10 seconds
        maxretry = 3 seconds
        [sshd]
            port = 3122
    [sshd-addos]
        port = 3122
        [dropbear]
            port = 3122
    [selinux-ssh]
            port = 3122
```
```bash
save the file
```
---

### restart service fail2ban

```bash
sytemcttl restart fail2ban.service
```