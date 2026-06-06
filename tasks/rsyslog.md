# rsyslog  

### server  

```bash
sudo apt update && sudo apt install rsyslog

#show more information
rsyslogd -v


systemctl status rsyslog
sudo systemctl start rsyslog

sudo vim /etc/rsyslog.conf

    # provides UDP syslog reception
    #module(load="imudp")
    #input(type="imudp" port="514")

    # provides TCP syslog reception
    #module(load="imtcp")
    #input(type="imtcp" port="514")
    #uncomment TCP and UDP  
```
```bash
#allow ufw
sudo ufw allow 514/tcp
sudo systemctl restart rsyslog.service  
```

---  

### client  

```bash
sudo apt update && sudo apt install rsyslog

#show more information
rsyslogd -v


systemctl status rsyslog
sudo systemctl start rsyslog


sudo vim /etc/rsyslog.d/50-default.conf

    *.* @@0.0.0.0:514
    *.* @@192.168.122.235
    cron.* @@192.168.122.237:514  
```
```bash
sudo systemctl restart rsyslog.service  
```

---  

### test  

```bash
logger 'test from client'
sudo tail /var/log/syslog  
```

---  

### ELK  

```bash
elastic search log stash kibana
vim /etc/logrotate.conf  
```

---  


### make file  

```bash
sudo touch /var/log/cron.log
sudo chmod 640 /var/log/cron.log
sudo chown syslog:adm /var/log/cron.log

sudo systemctl restart rsyslog

sudo vim /etc/rsyslog.d/50-default.conf
cron.* ===>> /var/log/cron.log
```