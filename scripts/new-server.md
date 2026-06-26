#!/bin/bash

##################################################################

countdown5() {
for i in {5..1}; do
	echo "$i"
	sleep 1
done
}

##################################################################

countdown3() {
for i in {3..1}; do
	echo "$i"
	sleep 1
done
}

##################################################################

echo -e "############################################################\nUpdating package list...\n############################################################"
apt update
echo -e "############################################################\nDONE!\n############################################################"

countdown3

echo -e "############################################################\ninstalling packages...\n############################################################"
apt install vim tree sudo ntpsec -y
echo -e "############################################################\nDONE!\n############################################################"

countdown5

echo -e "############################################################\nADD USER debian...\n############################################################"
sudo usermod -aG sudo debian
countdown3
sudo usermod -aG adm debian
cat /etc/group | grep sudo
cat /etc/group | grep adm
echo -e "############################################################\nDONE!\n############################################################"

countdown5

echo -e "############################################################\nADD KEY SSH...\n############################################################"
mkdir /home/debian/.ssh
countdown3
touch /home/debian/.ssh/authorized_keys
echo "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGE5U1fWN5XEZnHYNkPVoL5qnNlZZbA36kkBBmtxHgyN behnam@srv1" > /home/debian/.ssh/authorized_keys 
cat  /home/debian/.ssh/authorized_keys
echo -e "############################################################\nDONE!\n############################################################"

countdown5

echo -e "############################################################\nCONFIG NETWORK enp7s0\n############################################################"
touch /etc/network/interfaces.d/enp7s0
echo -e "\n\n##################### add by admin behnam ####################\n# 192.168.5.101 = route\n# 192.168.4.102 = NFS\nauto enp7s0\niface enp7s0 inet static\n\taddress 192.168.5.101\n\tnetmask 255.255.255.0\niface enp7s0 inet static\n\taddress 192.168.4.102\n\tnetmask 255.255.255.0" > /etc/network/interfaces.d/enp7s0
cat /etc/network/interfaces.d/enp7s0
echo -e "############################################################\nDONE!\n############################################################"

countdown3

echo -e "############################################################\nCONFIG NETWORK enp8s0\n############################################################"
touch /etc/network/interfaces.d/enp8s0
echo -e "\n\n#################### add by admin behnam ####################\n# 192.168.3.103 = NTP\n# 192.168.2.104 = SSH\nauto enp8s0\niface enp8s0 inet static\n\taddress 192.168.3.103\n\tnetmask 255.255.255.0\niface enp8s0 inet static\n\taddress 192.168.2.104\n\tnetmask 255.255.255.0" > /etc/network/interfaces.d/enp8s0
cat /etc/network/interfaces.d/enp8s0
echo -e "############################################################\nDONE!\n############################################################"

countdown3

echo -e "############################################################\nCONFIG NETWORK enp1s0\n############################################################"
sed -i '11,12s/^/# /' /etc/network/interfaces
echo -e "\n\n#################### add by admin behnam ####################\n# 192.168.1.100 = gateway\nauto enp1s0\niface enp1s0 inet static\n\taddress 192.168.1.100\n\tnetmask 255.255.255.0\n\tgateway 192.168.1.1\n\tdns-nameservers 8.8.8.8,4.2.2.4" >> /etc/network/interfaces
cat /etc/network/interfaces
echo -e "############################################################\nDONE!\n############################################################"

countdown5

echo -e "############################################################\nCONFIG SSH\n############################################################"
sed -i '14s/^#//' /etc/ssh/sshd_config
sed -i '16s/^#//' /etc/ssh/sshd_config
sed -i '33s/^#//' /etc/ssh/sshd_config
sed -i '35s/^#//' /etc/ssh/sshd_config
sed -i '36s/^#//' /etc/ssh/sshd_config
sed -i '38s/^#//' /etc/ssh/sshd_config
sed -i '57s/^#//' /etc/ssh/sshd_config
sed -i '58s/^#//' /etc/ssh/sshd_config
sed -i '109s/^/#/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '14,16,33,35,36,38,57,58,109s/^#/ //etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '90s/^/#/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '90s/^/#/' /etc/ssh/sshd_config\n############################################################"
sed -i '90s/^/#/' /etc/ssh/sshd_config
countdown3
sed -i '14s/22/4012/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '14s/22/4012/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '16s/0.0.0.0/192.168.2.104/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '16s/0.0.0.0/192.168.2.104/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '33s/prohibit-password/no/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '33s/prohibit-password/no/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '35s/6/3/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '35s/6/3/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '36s/10/1/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '36s/10/1/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '57s/yes/no/' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '57s/yes/no/' /etc/ssh/sshd_config\n############################################################"
countdown3
sed -i '109s|none|/etc/issue.net|' /etc/ssh/sshd_config
echo -e "############################################################\nsed -i '109s/none//etc//etc/issue.net/' /etc/ssh/sshd_config\n############################################################"
echo -e "############################################################\nDONE!\n############################################################"

countdown5


echo -e "############################################################\n/etc/issue.net\n############################################################"
echo -e "\n\n#################################################################################################
|		                   _    _           _   _                                       | 
|		                  / \  | | ___ _ __| |_| |                                      | 
|		                 / _ \ | |/ _ \ '__| __| |                                      | 
|		                / ___ \| |  __/ |  | |_|_|                                      | 
|		               /_/   \_\_|\___|_|   \__(_)                                      | 
|		                                                                                |  
|		  You are entering into a secured area! Your IP, Login Time,                    | 
|		   Username has been noted and has been sent to the server                      | 
|		                       administrator!                                           | 
|		   This service is restricted to authorized users only. All                     | 
|		            activities on this system are logged.                               | 
|		  Unauthorized access will be fully investigated and reported                   | 
|		        to the appropriate law enforcement agencies.                            | 
|                                                                                               | 
#################################################################################################\n\n" > /etc/issue.net
cat /etc/issue.net
countdown3
echo -e "\n\n#################################################################################################
|		                                                                                | 
|		                    This is a private server!                                   | 
|		           All connections are monitored and recorded.                          | 
|		     Disconnect IMMEDIATELY if you are not an authorized user!                  | 
|                                                                                               | 
#################################################################################################\n\n" > /etc/motd
cat /etc/motd
echo -e "############################################################\nDONE\n############################################################"

countdown5



echo -e "############################################################\nCHANGE HOST NAME\n############################################################"
sed -i '2s/srv12/srv100/' /etc/hosts
cat /etc/hosts | grep srv100
countdown3
sed -i 's/srv12/srv100/' /etc/hostname
cat /etc/hostname
echo -e "############################################################\nDONE\n############################################################"

countdown5


echo -e "############################################################\nCHANGE DNS\n############################################################"
sed -i '1s/^/# /' /etc/resolv.conf
sed -i '2s/^/# /' /etc/resolv.conf
sed -i '3s/^/# /' /etc/resolv.conf
echo 'nameserver 8.8.8.8' >> /etc/resolv.conf
echo 'nameserver 4.2.2.4' >> /etc/resolv.conf
cat /etc/resolv.conf
echo -e "############################################################\nDONE\n############################################################"

countdown5


echo -e "############################################################\nNTP SERVICE\n############################################################"
sed -i '34s/^/# /' /etc/ntpsec/ntp.conf
sed -i '35s/^/# /' /etc/ntpsec/ntp.conf
sed -i '36s/^/# /' /etc/ntpsec/ntp.conf
sed -i '37s/^/# /' /etc/ntpsec/ntp.conf
countdown3
echo -e '##################### add by admin behnam ####################\nserver 0.asia.pool.ntp.org\nserver 1.asia.pool.ntp.org\nserver 2.asia.pool.ntp.org\nserver 3.asia.pool.ntp.org\n############################################################\n' | sed -i '38r /dev/stdin' /etc/ntpsec/ntp.conf
cat /etc/ntpsec/ntp.conf | grep asia.pool
echo -e "############################################################\nDONE\n############################################################"

countdown5

