# common_cmd

# list changed files in last commit
git diff --name-only HEAD~1 HEAD

# find in multi folders and grep 
find /opt/asmslog/159/ /opt/asmslog/163/ /opt/asmslog/165/ -name 'asms-2019-05-08.log' |  xargs grep -E '执行XE失败'

# find files between specific times
find ./ -newermt "2019-05-31 17:08:00" -not -newermt "2019-05-31 17:09:00" | xargs grep -E 'CTU' | grep -E 'PEK' > /tmp/log.txt
[ubuntu-linux-find-files-between-specific-times](https://superuser.com/questions/580273/ubuntu-linux-find-files-between-specific-times)
