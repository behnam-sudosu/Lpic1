# change log directory  

```bash
vim /etc/logrotate.conf
vim /etc/logrotate.d
vim /etc/logrotate.d/nginx

#show where log is saved
/var/log/nginx/*.log
daily
rotate 14
compress
``` 