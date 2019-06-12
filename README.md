# common_cmd

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
