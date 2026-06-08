# systemctl

### you can set runleve

```bash
systemctl set-default runlevel
```

---

### you can see your runlevel

```bash
systemctl get-default runlevel
```

---

### start, stop, restart, reload, disable, enable, kill

```bash
# is better to use systemctl reload ssh
systemctl restart ssh
systemctl stop ssh
systemctl reload ssh
systemctl start ssh
systemctl disable ssh
systemctl enable ssh
systemctl status ssh
systemctl is-active ssh
systemctl is-enabled ssh
```

---

### install ssh

```bash
sudo apt install openssh-server
```

---

### show all services

```bash
systemctl
```

---

### save systemd file directory

```bash
# first direction save systemd
etc/systemd/system  
	# name service with .service
	file.service


# second directory save systemd
/usr/lib/systemd/system
	# name service with .service
	file.service

# for login user
/etc/profile.d
	# name service eith .sh
```

---

### systemctl information

```bash
# show where is load
Loaded: loaded (/usr/lib/systemd/system/nftables.service; disabled; preset: enabled)

# memory usage
Mem peak: 2.9M

# cpu usage
CPU: 38ms

# show logs
Jan 04 13:49:24 srv1 systemd[1]: Starting nftables.service - nftables...

# show logs
Jan 04 13:49:24 srv1 systemd[1]: Finished nftables.service - nftables...
```

---

### like systemctl and old sysadmin use this

```bash
service ufw status
```

---

### how type reboot

```bash
var/log/wtmp
```

# make file systemd service for linux

touch file.service

```bash
[Unit]
Description=nftables
Documentation=man:nft(8) http://wiki.nftables.org
Wants=network-pre.target
Before=network-pre.target shutdown.target
Conflicts=shutdown.target
DefaultDependencies=no

[Service]
Type=oneshot
RemainAfterExit=yes
StandardInput=null
ProtectSystem=full
ProtectHome=true
ExecStart=/usr/sbin/nft -f /etc/nftables.conf
ExecReload=/usr/sbin/nft -f /etc/nftables.conf
ExecStop=/usr/sbin/nft flush ruleset

[Install]
WantedBy=sysinit.target
```

save the file

---

```bash
# reload all services
systemctl daemon-reload
```