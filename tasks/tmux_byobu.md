# tmux  
	
### tmux help you if disconnect from server  

```bash
#install tmux
sudo apt install tmux

#run tmux
tmux

#after log out
#show how many window is open
#you can see you tmux session
tmux ls

#you can conect two people, 0 = which window is open
tmux att -t NUMBER OF SISSION
tmux new
tmux new-session
tmux kill-session -t NAME_SESSION

#close tmux
#exit
ctrl + d
```
```bash
note: you can use it for ping to check ping if you have packet lost
note: bring someone on server and teach them
```

# byobu  

### byobu help you if disconnect from server  

```bash
#install byobu
sudo apt install byobu
byobu

#use this for switch root
#when you switch to root otamaticly 
byobu-enable

#disable byobu
byobu-disable
byobo-select-backend

#short key
#Create a new window
F2

#Move to previous window
F3

#Move to next window
F4

#exit
ctrl + d
```