# common cmd

# list changed files in last commit
    git diff --name-only HEAD~1 HEAD

# find in multi folders and grep 
    find /opt/asmslog/159/ /opt/asmslog/163/ /opt/asmslog/165/ -name 'asms-2019-05-08.log' |  xargs grep -E '执行XE失败'

# find files between specific times
    find ./ -newermt "2019-05-31 17:08:00" -not -newermt "2019-05-31 17:09:00" | xargs grep -E 'CTU' | grep -E 'PEK' > /tmp/log.txt  
[ubuntu-linux-find-files-between-specific-times](https://superuser.com/questions/580273/ubuntu-linux-find-files-between-specific-times)

# List ports a process PID is listening on
    lsof -Pan -p PID -i  
[List ports a process PID is listening on (preferably using iproute2 tools)](https://unix.stackexchange.com/questions/157823/list-ports-a-process-pid-is-listening-on-preferably-using-iproute2-tools)

# Locate exact filename only
    locate -b '\AsmsBookOrderController.class'
[locate command for searching exact filename only](https://askubuntu.com/questions/831869/locate-command-for-searching-exact-filename-only)

# List all of files' size in current directory
    du -ah --max-depth=1 | sort -h
    du -sh -- * | sort -h
[how-do-you-sort-du-output-by-size](https://unix.stackexchange.com/questions/4681/how-do-you-sort-du-output-by-size)

# List folders size in current directory
    du -h --max-depth=1 | sort -h
[du-max-depth](https://www.peterbe.com/plog/du-max-depth)

# Find files that contains multiple specified strings   
    find . -type f  -exec grep -lZ FIND {} + | xargs -r0 grep -l ME
[how-to-search-files-where-two-different-words-exist](https://unix.stackexchange.com/questions/67794/how-to-search-files-where-two-different-words-exist)

    find . -type f -exec fgrep -q 'myString1' {} \; \
               -exec fgrep -q 'myString2' {} \; \
               -exec fgrep -q 'myString3' {} \; \
               -print
[recursively-locate-all-files-that-have-string-a-and-string-b-using-grep](https://stackoverflow.com/questions/22560705/recursively-locate-all-files-that-have-string-a-and-string-b-using-grep)  

# sqlplus logon remote oracle db as sysdba
    sqlplus sys/oracle@10.13.131.105:49161/xe as sysdba

# use a specific DNS server for querying a domain
    nslookup example.com 208.67.222.222 # nslookup example.com using the default DNS server
    dig @208.67.222.222 example.com #dig example.com using the default DNS server
[troubleshooting-dns-with-dig-and-nslookup](https://www.a2hosting.com/kb/getting-started-guide/internet-and-networking/troubleshooting-dns-with-dig-and-nslookup)

# get ip address
```shell
export IP_ADDR="$(ifconfig eth0 | awk '/inet / {print $2}')"
```
