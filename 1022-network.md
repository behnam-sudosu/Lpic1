# network

```bash
ip -br a
ip -br r
netpalan try
nat ===>> network address translation
IP ===>> internet protocol
DHCP ===>> Dinamic Host Configuration Protocol
```

```bash
vim /etc/netplan/*.yaml

	network:
	ethernets:
	ens33:
		dhcp4: false
		addresses:
			- 192.168.1.20/24
			- 192.168.1.21/24
		gateway4: 192.168.80.2
		nameservers:
			addresses: [8.8.8.8, 4.2.2.4]
	version: 2
```
```bash
network is unreachable ===>> biron nemire
destination host unreachable ===>> biron mire vali nemirese
```

---

### set DNS

```bash
# set DNS
/etc/resolv.conf

nameserver 8.8.8.8
nameserver 4.2.2.4

nameserver 185.206.92.250
nameserver 185.231.181.206

nameserver 194.104.158.78
nameserver 194.104.158.48
nameserver 216.85.97.202

nameserver 45.90.126.10
nameserver 45.90.33.120

nameserver 10.202.10.10
nameserver 10.202.10.11

nameserver 178.22.122.100
nameserver 185.51.200.2

nameserver 131.129.110.240
nameserver 185.51.200.2

nameserver 94.140.14.14
nameserver 94.140.15.15
```

### lock resolv.conf

```bash
sudo chattr +i /etc/resolv.conf
sudo chattr -i /etc/resolv.conf
```

---

### more information

```bash
nat = network address transportation
DHCP ===>> dinamic host configuration protocol
DNS server ===>> change IP to name
/etc/services ===>> show all ports
/etc/netplan/*.yamel ===>> ubuntu
/etc/network/interfaces ===>> debian
/etc/sysconfig/network-scripts/ifcfg-ens37 ===>> centos

# if you set here first come here and check then go /etc/resolve.conf
/etc/hosts
	192.168.1.100 google.com
	192.168.1.100 nginx.com
	192.168.1.200 srv2
	192.168.1.110 srv1
/etc/resolv.conf ===>> DNS server information
/etc/resolv.conf ===>> set DNS
/etc/nsswith.conf ===>> DNS check file in linux (hosts, resolve.conf, netplan)
DOH ===>> DNS over https
DOT ===>> DNS over tls
whois domain ===>> Get whois information for domains
```

---

### host

```bash
host ===>> go and ask what is the ip of google.com
host yahoo.com ===>> show IP
```

---

### commands

```bash
ip -br a ===>> show IP in systm
ip -br -c a ===>> show IP in systm with color
curl ===>> download from internet
curl myip-wtf/json ===>> show your IP
curl google.com === show IP google.com
```

---

### ifconfig

```bash
apt install net-tools
ifconfig ===>> network interface configuraton commands
ifconfig ===>> show all information about network
ifconfig -a ===>> show up and down network
ifconfig -s ===>> summery
ifconfig ens37 192.168.80.200 ===>> set static IP
ifconfig ens37 netmask 255.255.255.0 ===>> set static netmask
ifconfig ens37 192.168.80.200 netmask 255.255.255.0
ifconfig hw ens37 (mac address) ===>> change mac address
ifconfig ens38 up
ifconfig ens38 down
```

---

### if

```bash
# up and down network card
ifdown ens37
ifup eens37
```

---

### route

```bash
route ===>> show routing table
route ===>> show gateway
route -n ===>> show default gatway
route add default gw 192.168.1.100
route del default gw 192.168.1.100  
route add default gw 192.168.1.100 dev ens37
route del default gw 192.168.1.100 dev ens37
```

---

### ip

```bash
ip address show ===>> show interface
ip addr sh
ip a s
ip a
```
```bash
ip addr add 192.168.1.100/24 dev ens37 ===>> add ip
ip addr del 192.168.1.100/24 dev ens37 ===>> delete ip
```
```bash
ip link show ===>> show disable and enable
ip link set ens37 down
ip link set ens37 up
```
```bash
ip route show
ip ro sh
ip r s
ip route add 10.0.0.0 via 172.160.100 dev ens37 ===>> if you want say where you have to go out
ip route del 10.0.0.0 via 172.160.100 dev ens37
ip route add default via 192.168.1.1 dev ns37
ip route del default via 192.168.1.1 dev ns37
```

---

### ping

```bash
apt install iputils-ping
ping google.com
ping 8.8.8.8
ping -c 3
ping -i 0.5 ===>> second
ping -I ens37 ===>> choose interface give me ping
ping -a  ===>> alarm
ping -s ===>> size
```

---

### troubleshoot

```bash
traceroute ===>> show path
traceroute 8.8.8.8

tracepath ===>> show path
tracepath 8.8.8.8

mtr ===>> show path
mtr yahoo.com
```

---

### netstat

```bash
ESTABLISHED ===>> conected
LISTEN ===>> ready for connect
```
```bash
netstat ===>> show all connection in your network
netstat ===>> show network connection
netstat -a ===>> all
netstat -at ===>> tcp
netstat -au ===>> udp
netstat -l ===>> list
netstat -n ===>> port number
netstat -p ===>> pid  
netstat -rn = like a route -n
```

---

### ss

```bash
ss -a ===>> all
ss -at ===>> tcp
ss -au ===>> udp
ss -l ===>> list
ss -n ===>> port
s -p ===>> pid  
```

---

### telnet

```bash
telnet 192.168.1.100 22 ===>> show port 22 is exist or open on server and application is active
netcat -l 8080 ===>> you can open port (server)
telnet 192.168.1.100 8080 ===>> connect to server port
telnet google.com 80 ===>> connect to port 80 google.com and you know port 80 is open in google.com
```

---

### nc or netcat

```bash
netcat ===>> open port in linux

# server
netcat -l 8090

# client
telnet IP_SERVER 8090
```

---

### transfer file

#### server

```bash
nc -l 8080
nc -l -p 9000 > file1.txt ===>> file transfer
```

#### client

```bash
nc server_IP 9000 < file1.txt ===>> file transfer
```
```bash
nc -l 8990 ===>> port you can talk (net cat)
	nc 8990 (ip destination)
```

---

### nslookup

```bash
nslookup google.com
nslookup ===>> go and ask what is the ip of google.com
nslookup @8.8.8.8.8 google.com
nslookup
	server 1.1.1.1 ===>> change dafault nslookup server
	8.8.8.8
	google.com
```

---

### dig

```bash
dig ===>> show DNS information and records
dig ===>> go and ask what is the ip of google.com
dig DOMAIN_NAME ===>> Get DNS information for domain
dig yahoo.com +short ===>> show only IP
dig -x HOST ===>> Reverse lookup host
dig yahoo.com
dig nginx.com
dig yahoo.com +short ===>> only show IP without information  
```

---

### dhclient

```bash
dhclient ===>> take ip in DHCP
dhclient -v ens37
dhclient -r ===>> remove configuration
```