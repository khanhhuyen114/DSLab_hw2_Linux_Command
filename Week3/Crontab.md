theia@theia-many37758:/home/project$ crontab -l
no crontab for theia
theia@theia-many37758:/home/project$ crontab -e
no crontab for theia - using an empty one
crontab: installing new crontab
theia@theia-many37758:/home/project$ crontab -l
# Edit this file to introduce tasks to be run by cron.
# 
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
# 
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use '*' in these fields (for 'any').# 
# Notice that tasks will be started based on the cron's system
# daemon's notion of time and timezones.
# 
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
# 
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
# 
# For more information see the manual pages of crontab(5) and cron(8)
# 
# m h  dom mon dow   command
0 21 * * * echo "Welcome to cron" >> /tmp/eho.txt

theia@theia-many37758:/home/project$ chmod u+x diskusage.sh
theia@theia-many37758:/home/project$ ./diskusage.sh
Tue Sep 12 13:35:07 EDT 2023
Filesystem      Size  Used Avail Use% Mounted on
overlay          98G   53G   41G  57% /
tmpfs            64M     0   64M   0% /dev
tmpfs            16G     0   16G   0% /sys/fs/cgroup
/dev/vda2        98G   53G   41G  57% /etc/hosts
shm              64M     0   64M   0% /dev/shm
tmpfs            28G   16K   28G   1% /run/secrets/kubernetes.io/serviceaccount
tmpfs            16G     0   16G   0% /proc/acpi
tmpfs            16G     0   16G   0% /proc/scsi
tmpfs            16G     0   16G   0% /sys/firmware
theia@theia-many37758:/home/project$ crontab -e
crontab: installing new crontab
theia@theia-many37758:/home/project$ crontab -l
# Edit this file to introduce tasks to be run by cron.
# 
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
# 
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use '*' in these fields (for 'any').# 
# Notice that tasks will be started based on the cron's system
# daemon's notion of time and timezones.
# 
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
# 
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
# 
# For more information see the manual pages of crontab(5) and cron(8)
# 
# m h  dom mon dow   command
0 21 * * * echo "Welcome to cron" >> /tmp/eho.txt

0 0 * * * /home/project/diskusage.sh >> /home/project/diskusage.log
theia@theia-many37758:/home/project$ ls
array.sh          column_3.txt           diskusage.sh  script.sh
arrays_table.csv  conditional_script.sh  report.csv    total.sh
theia@theia-many37758:/home/project$ crontab -r
theia@theia-many37758:/home/project$ crontab -l
no crontab for theia
theia@theia-many37758:/home/project$ crontab -e
no crontab for theia - using an empty one
crontab: installing new crontab
theia@theia-many37758:/home/project$ crontab -l
# Edit this file to introduce tasks to be run by cron.
# 
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
# 
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use '*' in these fields (for 'any').# 
# Notice that tasks will be started based on the cron's system
# daemon's notion of time and timezones.
# 
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
# 
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
# 
# For more information see the manual pages of crontab(5) and cron(8)
# 
# m h  dom mon dow   command
* * * * * date >> /tmp/everymin.txt
theia@theia-many37758:/home/project$ 