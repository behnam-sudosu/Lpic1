# ssh

### install package
```bash
apt install openssh-server -y
apt install openssh-client -y
private key ===>> for client
public key ===>> for server
```

---

### generate sshkey nad copy to server

```bash
ssh-keygen ===>> generate ssh keygen
ssh-copy-id milad@192.168.1.4
ssh behnam@192.168.1.100
vim /home/behnam/.ssh/id_rsa.pub ===>> copy ssh public key
/home/behnam/.ssh/authorized_keys ===>> past public key here
```

---

### script on client for ssh

```bash
you can ssh without username and paswword
cd .shh
make file vim config
	Host databases-1
		HostName 192.168.1.4
		User behnam
		Port 22
		IdentityFile ~/.ssh/id_ed25519 ===>> directory key
		IdentitiesOnly yes ===>> use this key only
```
```bash
save the file
ssh database-1
```

---

```bash
Host *
	User behnam
	Port 22
```

---

### make this file if you work for many company

```bash
/home/behnam/.ssh/config
	include /home/behnam/.ssh/config.d/*.conf ===>> this goese check all
```
```bash
save the file
```
```bash
mkdir config.d
vim mci-conf
	Host databases-1
		HostName 192.168.1.4
		User behnam
		Port 22

	Host databases-2
		HostName 192.168.1.4
		User behnam
		Port 22
```
```bash
save file
```

---

```bash
vim bmi.conf
	Host srv-1
		HostName 192.168.1.4
		User behnam
		Port 22

	Host srv-2
		HostName 192.168.1.4
		User behnam
		Port 22
```
```bash
save the file
```

---

### ssh on server

```bash
vim /etc/ssh/ssh-config ===>> for client
vim /etc/ssh/sshd-config ===>> for server
	port 22 ===>> change port
	addresssfamily ipv4or ipv6
	listen address 192.168.80.100 ===>> interface listen
	Authentication
	loginGraceTime 2M ===>> after 2m logout outomatic
	PermitRootLogin ===>> root can login (no)
	MaxAuthTries ===>> how many times you can type password wrong
	MaxSssions ===>> how many pepople can login with ssh
	PublicKeyAuthentication (yes) ===>> can login with public key
	PasswordAuthentication (no) ===>> 
	sshd-config ===>> you can set yes or no
	x11 forwardin ===>> make it command
```
```bash
save the file

vim /etc/ssh/sshd.config.d/*.conf ===>> chane passwordAuthentication no

systemctl restart sshd
```

---

# make keygen

```bash
ssh-keygen -t ed25519 -C "your_email"
ssh_keygen -t rsa -b 4096 -C "your_email"
ssh-keygen -t ed25519 -C "git@gitlab.com" -f ~/.ssh/id_ed25519_gitlab
ssh-keygen -t ed25519 -C "git@github.com" -f ~/.ssh/id_ed25519_github
ssh-keygen -t rsa -b 4096 -C "git@gitlab.com" -f ~/.ssh/id_rsa_gitlab
ssh-keygen -t rsa -b 4096 -C "git@github.com" -f ~/.ssh/id_rsa_github
```

---

```bash
touch config
	Host git.gitlab.com
		HostName git.gitlab.com
		User git
		IdentityFile ~/.ssh/id_ed25519_gitlab
	
	Host git.hub.com
		HostName git.hub.com
		User git
		IdentityFile ~/.ssh/id_ed25519_github
```
```bash
save the file
```

---

```bash
chmod 600 ~/.ssh/config
chmod 600 ~/.ssh/id_ed25519_gitlab
chmod 600 ~/.ssh/id_ed25519_github
```

---

```bash
# check for connection
ssh -T git@github.com
ssh -T git@gitlab.com
```

---

```bash
# make config for git
vim ~/.ssh/config.d/*.conf
	Host gitlab.com
	HostName gitlab.com
	User git
	IdnetityFile ~/.ssh/id_ed25519_gitlab

vim ~/.ssh/config.d/*.conf
	Host github.com
	HostName github.com
	User git
	IdnetityFile ~/.ssh/id_ed25519_github
```
```bash
save the file
```

---

```bash
# check which keys for gitlab and github
ssh -vT git@gitlab.com
ssh -vT git@github.com
```