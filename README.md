"# bashscripting" 

### Clean Up Log files 
``` Bash Script
LOG_DIR=/var/log
cd $LOG_DIR
rm-rf  $LOG_DIR
```
### Check if user has Permission
``` Bash Script
if ["$UID" -ne 0]
then 
  echo "Must be root to run"
fi 
```

### Check if command line arguments are passed 
``` Bash Script
if [ -n "$1" ]
then 
  echo 'Values Passed'
else 
  echo "Values not passed"
fi 
```
### Show Data & Time , List all Looged users   , Give system Uptime , Save this to log file
``` Bash Script 
loc =/var/log
filename = $1
cd $loc
date>>$filename
uptime>>$filename
who>>&filename


```

