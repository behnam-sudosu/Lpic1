# NTP server  

### server  

```bash
ntp ===>> network time protocol
site = ntppool.org ===>> you can use this site for set time

#befor install ntp
apt install ntpdate
ntpdate -v pool.ntp.org
ir.pool.ntp.org
```

---      

### install

```bash
apt update && apt install ntp

#same as ntp
apt install chrony

#in debian
apt install ntpsec
```

---  

### config file

```bash
systemctl status ntp.service

#show information
ntpq -p
vim /etc/ntp.conf
    pool 192.168.1.100 iburst
    pool ir.pool.ntp.org iburst
systemctl restart ntp  
```

---  

### client  

```bash
apt update && apt install ntp
vim /etc/ntp.conf
    poll 0.ubuntu.pool.ntp.org iburst
    pool 192.168.1.100 iburst
systemctl restart ntp
ntpq -p
```