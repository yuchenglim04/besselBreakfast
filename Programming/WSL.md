**Check WSL version via Windows command prompt**  
`wsl -l -v`

**Programmes downloaded in Windows vs in WSL**  
`jupyter      # WSL`  
`jupyter.exe  # Windows`  
Try `which` to find out  

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
```
sudo mkdir /mnt/d                      # choose a matching letter to your drive
sudo mount -t drvfs D: /mnt/d
```
https://askubuntu.com/questions/1116200/how-can-i-access-my-usb-drive-from-my-windows-subsystem-for-linux-ubuntu-dist  
It's nice when references are given  
https://askubuntu.com/questions/1454199/how-can-i-mount-a-removable-usb-drive-in-wsl
