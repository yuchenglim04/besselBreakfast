**. vs ..**  
```
ls -aF                  # you'll see ./ and ../
cd .                    # so . and .. are treated as directories in your folder!
```
**color, highlighting and ls**  
Changing the color!!  
https://unix.stackexchange.com/questions/94498/what-causes-this-green-background-in-ls-output  

**super user**  
```
id                # check your permissions
sudo su           # trigger superuser
id
Crtl + D          # to leave superuser
```

**where you are right now**  
`pwd`  

**linux home directory**  
`cd`  
`cd ~`  
To see what's there, try `ls -a`  

**Where does pip install its packages?**  
```
/home/normaluser/.local/lib..
/ root/.local/lib..
pip list -v
```
https://stackoverflow.com/questions/29980798/where-does-pip-install-its-packages  
https://stackoverflow.com/questions/77344542/how-to-ensure-pip-is-installing-dist-info-rather-than-egg-info  
https://stackoverflow.com/questions/2051192/what-is-a-python-egg?answertab=modifieddesc#tab-top  
https://stackoverflow.com/questions/20994716/what-is-the-difference-between-pip-and-conda/68897551#68897551  
https://stackoverflow.com/questions/9387928/whats-the-difference-between-dist-packages-and-site-packages  
https://stackoverflow.com/questions/2927993/where-are-the-python-modules-stored  


**Where can I find the location of folders for installed programs?**  
`which <command>`  
https://askubuntu.com/questions/54395/where-can-i-find-the-location-of-folders-for-installed-programs

**list of all commands**  
`compgen -c`  
`compgen -c | grep 'ctl$'`  
https://unix.stackexchange.com/questions/94775/list-all-commands-that-a-shell-knows  
https://unix.stackexchange.com/questions/395230/how-to-search-available-commands-in-bash

**Jupyter Lab**  
Config files are stored by default in the ~/.jupyter directory.

**About programmes/commands installed**  
```
pip list
pip show <package_name>
apt list --installed
apt show <package name>
man <command>
help <command>
lsb_release -a          # print all info  
lsb_release -b          # print one line only

cd /etc
ls *os*
cat os-release
```


**Python**  
```
import numpy as np
np.__version__
np.__file__                     # gives file location
dir(np)                         # all attributes/methods
help(np)                        # prints the help, super long, not useful 
```
https://stackoverflow.com/questions/247770/how-to-retrieve-a-modules-path  
https://stackoverflow.com/questions/5103329/how-to-find-out-what-methods-properties-etc-a-python-module-possesses  

# Future topics
`alias`
