This introduction will provide insights into the operation of Linux. It will not explain the commands used. The commands are placed in a separate cheat sheet instead. The idea is that you should learn the commands as building-blocks, then combine them in a creative way to achieve your goals.

There are many cheat sheets online. But always try to make one for yourself, tailored for your work! We will provide our personal sheets so that you can get started right away.

Also, make your own help files or tutorials for yourself. Different sources give different examples. Some might be inspirational to you, but dull to someone else. So copy and paste links, examples, tips and tricks into your very own 'tutorial'. Someday you might share it out. But perhaps there's no need to, given the sheer number of very useful ones out there. Anyway, make your own notes.

# Learning Linux the "Open Every Door", "Clicking Every Button" Way

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

Bash scripting  
[Advanced Bash-Scripting Guide](https://tldp.org/LDP/abs/html/)  
[Bash Reference Manual](https://www.gnu.org/software/bash/manual/bash.html)

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
var                    # your there's a folder 'log' that contains system logs
```



# Establising workflows
## Installing packages
## compiling code (C, C++)
## auto backup
## auto upload to Github
## mounting, unmounting devices

