This introduction will provide insights into the operation of Linux. It will not explain the commands used. The commands are placed in a separate cheatsheet instead. The idea is that you should learn the commands as building-blocks, then combine them in a creative way to achieve your goals.

# Learning Linux the "Open Every Door Way"

# How to learn Linux: have you ever wondered how people write tutorials?
- Primary sources:
  - Linux gurus
  - Manuals/Help!

Online manuals: compare the different visual rendering and depth of explanations:

man.he.net : comprehensive (verbose?), pure ascii so hard to read!   
http://man.he.net/?topic=tar&section=all  
man7.org : comprehensive (verbose?), HTML rendering :)  
https://man7.org/linux/man-pages/man1/tar.1.html  
commandlinux.com : straight to the point, but less explanation  
https://www.commandlinux.com/man-page/man1/tar.1.html  

ss64.com : comprehensive; even has examples!  
https://ss64.com/bash/echo.html  
vs  
https://www.man7.org/linux/man-pages/man1/echo.1.html

Offline manuals: (knowing vi navigation keys helps a lot! Also, pay attention to white strip at bottom!)
```
help
help help   
help cat                #-bash: help: no help topics match `cat'.  Try `help help' or `man -k cat' or `info cat'.
man cat
info cat
```

# Exploring the filesystem
root: /  
home: ~  
```
cd                    # to home
cd ~                  # to home
cd /                  # to root
```

Try going to root, then display the folders and files there (try ls, then ls -a).

Several important folders:  
```
bin
dev
home
mnt
```



