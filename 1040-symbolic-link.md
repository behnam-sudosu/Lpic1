# link  

```bash
symbolic link ===>> shortcut, pointer
```

### hardlink  

```bash
defrence
	1-inod is same
	2-you can't link direcroty just file
	3-change permision
	4-if delete original file the link of file work it  
```

```bash
#show inod
df -i

ln FILE_SOURCE LOCATION_OF_LINK

#unlink
unlink hardlink

vim file1
	devops

#show innod
ls -li
```

---  

### softlink  

```bash
difrence
	1-inod is not same
	2-you can link directory
	3 dosen't change permision
	4-delete orginal file the link is dosn't work
```

```bash
#softlink
ls -s FILE_SOURCE LOCATION_OF_LINK
ln -s file1

#unlink
unlink softlink

#you can rm file also
rm FILE NAME
```
