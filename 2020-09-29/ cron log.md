###  cron log


[Where is the cron / crontab log? - Ask Ubuntu](https://askubuntu.com/questions/56683/where-is-the-cron-crontab-log "Where is the cron / crontab log? - Ask Ubuntu")


 

```
/var/log/syslog
tail -f /var/log/syslog | grep CRON

```
