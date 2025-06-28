**To backup (perhaps in a script file; remove the comments!):**
```
 tar \
--exclude='pico/pico-sdk' \                                    # excluding large files that I don't need
--exclude='pico/pico-examples'  \
--exclude='./.*' \                                            # if ".", will exclude current directory!
--exclude='projects/opencv' \
--exclude='projects/opencv_contrib' \
-zcvf /mnt/d/project_files_$(date +%Y%m%d).tar.gz . \        # "." current directory # -z to compress
```

**To check backup:**
```
tar -tf tar_file                                             # -f is needed for tar to open the file
tar -ft tar_file                                             # doesn't work! Because the file name is the parameter for the flag -f, so parameter must follow flag
tar -tvf tar_file  | more                                    # -v verbose ; |more for pagination
```

**To extract**
```
cd target_directory
tar -xvf path/tar_file.tar.gz                                # extract all
tar -xvf ../tar_file.tar.gz ./what_you_want                    # if you archived .
tar -xvf ../tar_file.tar.gz compressed_folder_name/what_you_want    # if you archived a folder
```

```
gzip file
gunzip file.gz
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
**Becareful: extracting to linux/usb**  
Error "Cannot utime: Operation not supported" when restoring a tar archive on an android device  
https://askubuntu.com/questions/631562/error-cannot-utime-operation-not-supported-when-restoring-a-tar-archive-on-an  

</br>
</br>

**How to use date correctly**
```
date
date +20%y%m%d
date +%y%m%d
date +%Y%m%d
date +%m
date %Y%m%d            #error
```


**What won't work**
```
tar --exclude='folder1' -cvf my.tar folder1 folder2                 # works
tar --exclude=folder1 -cvf my.tar folder1 folder2                 # works
tar --exclude='folder1/' -cvf my.tar folder1 folder2                # fails
```
