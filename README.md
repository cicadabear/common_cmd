# common_cmd

# list changed files in last commit
git diff --name-only HEAD~1 HEAD

# find in multi folders and grep 
find /opt/asmslog/159/ /opt/asmslog/163/ /opt/asmslog/165/ -name 'asms-2019-05-08.log' |  xargs grep -E '执行XE失败'

