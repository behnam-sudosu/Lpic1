# config network Ubuntu

### set ip static for ubuntu  

```bash
cd /etc/netplan/*.yaml

    # Let NetworkManager manage all devices on this system
    network:
        version: 2
        rendere: NetworkManager
        etherents:
        enp0s25:
            dhcp4: false 
            addresses:
            - 192.168.1.100/24
            gateway4: 192.168.1.1
            nameservers:
                addresses: [8.8.8.8, 1.1.1.1]
```
```bash
save the file
sudo netplan try or sudo netplan apply 
```

---  

### Set NameServers  

```bash
    cd /etc
    resolv.conf is a link in ubuntu 22.4
    remove resolv.conf
    sudo unlink resolv.conf
    touch /etc/resolv.conf
    vim resolv.conf
        nameserver 8.8.8.8
        nameserver 4.2.2.4
```
```bash
    save the file
    also you can add nameserver to /etc/netplan/*.yaml too
```

---  

### route  

```bash
use route insted of getway
routes:
    - to: default
    via: 192.168.0.1
```