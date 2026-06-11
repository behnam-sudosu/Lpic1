# config network Debian

### set ip static for debian

```bash
cd /etc/network
vim interfaces
```
```bash
# The loopback network interface
auto lo
iface lo inet loopback
# The primary network interface
auto ens36
iface ens36 inet static
        address 192.168.1.100/24
        netmask 255.255.255.0
        gateway 192.168.1.1
        dns-nameservers 8.8.8.8
```
```bash
save the file  
sudo systemctl restart networking.service
```

---

### set ip with sub

```bash
auto ens36:0
iface ens36:0 inet static
        address 192.168.1.101/24
        netmask 255.255.255.0
```

---

### set nameservers

```bash
cd /etc
vim resolv.conf
```
```bash
nameserver 8.8.8.8
nameserver 4.2.2.4
```
```bash
save the file
```