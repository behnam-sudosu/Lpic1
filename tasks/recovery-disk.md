# recovery disk

### ext

```bash
fsck ===>> check disk for error
    check inod
    check bad sector
    directory structure


fsck file system check ===>> use for ext
fsck.ext4 /dev/sdb1 ===>> befor that unmunt
fsck -t ext4 /dev/sdb1 ===>> check disk
fsck -n ===>> just check
fsck -f ===>> force fix
fsck -f /dev/sdb1 -y ===>> fix it
```
```bash
tune2fs ===>> check disk for error

tune2fs -l /dev/sdb1
```
```bash
dumpe2fs ===>> check disk for error

dumpe2fs /dev/sdb1 ===>> show superblock
```

---

### xfs

```bash
xfsdump
xfsrepair
xfsinfo
xfsrestore
xfscheck
```