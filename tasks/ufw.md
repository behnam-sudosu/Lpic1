# ufw

```bash
# change setting
vim /etc/default/ufw
```

---

### enable ufw

```bash
sudo ufw version
sudo ufw status
    status: inactive
sudo ufw enable
sudo ufw disable
```

---

### set rules

```bash
sudo ufw default allow outgiung
sudo ufw default allow incoming
sudo ufw default deny outgoing
sudo ufw default deny incoming

sudo ufw allow OpenSSH
sudo ufw deny OpenSSH
sudo ufw allow ssh
sudo ufw deny ssh
sudo ufw allow 22
sudo ufw deny 22

sudo ufw allow from IP_ADDRESS
sudo ufw deny from IP_ADDRESS
sudo ufw allow from IP_ADDRESS/24
sudo ufw deny from IP_ADDRESS/24
sudo ufw allow from IP_ADDRESS to any port 22
sudo ufw deny from IP_ADDRESS to any port 22
sudo ufw allow from IP_ADDRESS/24 to any port 22
sudo ufw deny from IP_ADDRESS/24 to any port 22
sudo ufw allow in on eth37 to any port 80
sudo ufw deny in on eth37 to any port 80
```

---

### check

```bash
sudo ufw app list
sudo ufw status numbered
sudo ufw show added
```

---

### delete command

```bash
sudo ufw delete [number]
sudo ufw delete allow "Apache Full"
sudo ufw delete allow http
sudo ufw delete allow 80
```

---

### reset command

```bash
    sudo ufw reset
```