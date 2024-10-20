**To backup:**
```
 tar \
--exclude='pico/pico-sdk' \
--exclude='pico/pico-examples'  \
--exclude='./.*' \                                            # if ".", will exclude current directory!
--exclude='projects/opencv' \
--exclude='projects/opencv_contrib' \
-zcvf /mnt/d/project_files_$(date +%Y%m%d).tar.gz . \        # "." current directory
```

**To check backup:**
```
tar -tf tar_file                                             # -f is needed for tar to open the file
```

### Read the docs
short  
https://www.commandlinux.com/man-page/man1/tar.1.html  
long: what's the point with -f
https://www.gnu.org/software/tar/manual/html_node/file-tutorial.html#file-tutorial

</br>
</br>

**Backup specific folders**
https://askubuntu.com/questions/978795/using-tar-to-only-backup-specific-folders  
**Exclude folders**  
https://stackoverflow.com/questions/984204/shell-command-to-tar-directory-excluding-certain-files-folders  
**Backup the whole of current directory**  
https://stackoverflow.com/questions/3651791/tar-add-all-files-and-directories-in-current-directory-including-svn-and-so-on  
**Exclude hidden files**  
https://stackoverflow.com/questions/20487843/how-to-make-tar-exclude-hidden-directories  
**Single command, multiple lines**  
https://superuser.com/questions/508507/linux-bash-script-single-command-but-multiple-lines  

</br>
</br>

**how to use date correctly**
```
date
date +20%y%m%d
date +%y%m%d
date +%Y%m%d
date +%m
date %Y%m%d            #error
```
