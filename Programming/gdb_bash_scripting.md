**A syntax error**  
wrong:
```
(sleep 2;echo I am 2) &;(sleep 1;echo  I am 1) &;(sleep 3; echo I am last) &
```
output:
```
-bash: syntax error near unexpected token `;'
```
right:
```
((sleep 2;echo I am 2;) &) ; ((sleep 1;echo  I am 1;) &) ; ((sleep 3; echo I am last;
) &) ;
```

wrong: `local cmd = $1`  
right: `local cmd=$1`  

</br>
</br>

## 4 ways to make a GDB 'script'
### 1 Gives a plus before the command shown...
```
#run programme and provide input from shell script
#https://stackoverflow.com/questions/64000750/running-program-and-providing-input-from-shell-script

{
echo set trace-commands on
echo break main
echo disassemble main
echo run
echo -e "info registers \n c\n"
echo quit
} | gdb a.out -q
```
### 2 Best output, as if you actually type in the commands
```
#Useful batch trick and Color Code logging
#https://stackoverflow.com/questions/27397865/how-to-write-stdout-to-file-with-colors
#http://www.etalabs.net/sh_tricks.html
#https://sentry.io/answers/check-that-a-string-contains-a-substring-in-bash/


gdb_wait() {

local matchString=$1
local delimSeparator="b) "

while read -d "$delimSeparator" line <&4; do
        if [[ $line == *"$matchString"* ]]; then
                break
        fi
done

}

gdb_run() {

local cmd=$1
echo $cmd
echo $cmd >&3

}

mkfifo IN OUT

(script -q -c "gdb -q "$1" <IN" | tee -a OUT) &
exec 3> IN 4< OUT
gdb_wait '(gd'
gdb_run 'disassemble main'
gdb_wait '(gd'
gdb_run 'run'
gdb_wait '(gd'
gdb_run 'q'

rm IN OUT
```
### 3 Load a bunch of commands from a file
https://stackoverflow.com/questions/14226563/how-to-read-and-execute-gdb-commands-from-a-file
### 4 Official, but complicated GDB scripting
https://sdimitro.github.io/post/scripting-gdb/

</br>
</br>

## Background reading:  
**Homework: read the docs!**  
https://ss64.com/bash/read.html  
https://ss64.com/bash/source.html   
https://ss64.com/bash/echo.html  

**Indent multiple lines quickly in vi**  
https://stackoverflow.com/questions/235839/indent-multiple-lines-quickly-in-vi  

**echo '\n'**  
https://www.uptimia.com/questions/how-to-simulate-an-enter-keypress-in-a-bash-script  

**Single command, multiple lines**  
https://superuser.com/questions/508507/linux-bash-script-single-command-but-multiple-lines  

**How to use echo to run commands**  
https://stackoverflow.com/questions/17674137/can-i-use-echo-to-execute-commands  

**Problem: when feeding input, the programme does not echo back the input**  
https://stackoverflow.com/questions/1707167/how-to-dump-the-entire-gdb-session-to-a-file-including-commands-i-type-and-thei  


