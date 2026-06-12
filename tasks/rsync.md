# rsync

### rsysnc help for copy from local to server

```bash
sudo apt install rsync
copy from server
rsync -a ===>> copy file with all permision
rsync -v ===>> show information
rsync -z ===>> zip file
rsync -h ===>> human readable
```

---

```bash
rsync -zvh mydir.tar /tmp
rsync -azvh mydir /tmp ===>> a == directory move
rsync -azvh mydir behnam@192.168.1.100:/tmp ===>> copy to another server
rsync -azvh behnam@192.168.1.100:/tmp/mydir /tmp
rsync -azvh --max-size='200k' mydir behnam@192.168.1.100:/tmp ===>> server transfer file
rsync -azvh --bwlimit=100 mydir behnam@192.168.1.100:/tmp ===>> bandwith limit 
rsync -azvh --remove-source-file mydir behnam@192.168.1.100:/tmp ===>> delete source file
```