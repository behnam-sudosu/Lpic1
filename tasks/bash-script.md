# bash script advance

```bash
echo "Hello world!"
touch app.sh ===>> postfix must be (sh)
chmod +x NAME_FILE
open file with vim
```
```bash
#!/bin/bash ===>> start file with this command
#!/usr/bin/ env bash ===>> use this is better
```
```bash
excute file
1---->> ./NAME_FILE
2---->> /bin/bash NAME_FILE
3---->> bash NAME_FILE
4---->> sh NAME_FILE
```

---

### scripts

```bash
app.sh
	v1=world
	printf "hello, $v1"

app1.sh
	echo "Who are you"
	read name ===> take valu from users
	echo "Hello, $name"
```

---

### if

```bash
v1=2000
v2=200
if [[ condition ]];then
	statement
elif [[ condition ]]; then
	statement
else
	statement
if [[ condition && condition ]];then ===>> all must be true
	statement
if [[ condition || condition ]];then ===>> only one must be true
	statement
```

---

### for

```bash
first
	arr=(a b c d e f g)
	for i in "${arr[@]}"; do
		echo $i
	done
	
second
	#!/bin/bash
	arr=(a b c d e f g)
	for (( i=0; i<${#arr[@]}; i++ )); do
		echo ${arr[$i]}
	done
	
hints
	for i in {1..10}; do
		echo $i
	done
```

---

### while

```bash
first
	arr=(a b c d e f g)
	i=0
	while [[ $i -lt ${#arr[@]} ]]; do
		echo ${arr[$i]}
		i=$(expr $i + 1)
		i=$i+1
	done

second
	arr=(a b c d e f g)
	i=0
	while [[ $i < ${#arr[@]} ]]; do
		echo ${arr[$i]}
		((i++))
	done

# show time
for (( i = 1 ; i <= 10 ; i++ )); do
	echo "The date and time is $(date)"
	sleep 5
done
```