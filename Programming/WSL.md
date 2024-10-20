**Check WSL version via Windows command prompt**  
`wsl -l -v`

**Programmes downloaded in Windows vs in WSL**  
`jupyter      # WSL`  
`jupyter.exe  # Windows`  
Try `which` to find out  
  asd
**File system**  
`/mnt/c/Users/user_name/      # Windows`  
`~/                           # WSL`

**To open a WSL folder in Windows file explorer**  
`explorer.exe ..`

**To automatically start WSL from home!**  
`Ctrl + ,      # short cut for settings`  
`              # choose startup > default profile > Tux mascot ubuntu`   
This gave me the idea, but I did not follow it all the way! I opended the settings and hit gold!  
https://broersma.dev/how-to-start-wsl-in-linux-user-home/  


**Mount USB**  
Apparently Windows has already mounted the USB, but WSL jsut can't 'see' it. Even blkid can't.
```
sudo mkdir /mnt/d                      # choose a matching letter to your drive
sudo mount -t drvfs D: /mnt/d
sudo umount d                          # still have to eject via Windows; the folder d is still there; notice the changes in highlighting
```
The real linux way:
```
sudo blkid                             # try before and after plugging the drive
lsblk
df -hT                                 # check space
```

https://askubuntu.com/questions/1116200/how-can-i-access-my-usb-drive-from-my-windows-subsystem-for-linux-ubuntu-dist  
It's nice when references are given  
https://askubuntu.com/questions/1454199/how-can-i-mount-a-removable-usb-drive-in-wsl

Try reading the docs: too much info??  
http://man.he.net/?topic=mount&section=all  
Another docs: too much info missing  
https://ss64.com/bash/mount.html  
