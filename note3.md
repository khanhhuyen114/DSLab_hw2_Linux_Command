theia@theia-many37758:/home/project$ ls -l greet.sh
-rw-r--r-- 1 theia users 522 Sep 12 00:05 greet.sh
theia@theia-many37758:/home/project$ bash greet.sh
Enter your name :Huyen
Welcome Huyen
Congratulations! You just created and ran your first shell script using Bash on IBM Skills Network
theia@theia-many37758:/home/project$ which bash
/bin/bash
theia@theia-many37758:/home/project$ chmode +x greet.sh
bash: chmode: command not found
theia@theia-many37758:/home/project$ chmod +x greet.sh
theia@theia-many37758:/home/project$ chmod u+x greet.sh
theia@theia-many37758:/home/project$ ls -l greet.sh
-rwxr-xr-x 1 theia users 535 Sep 12 00:07 greet.sh
theia@theia-many37758:/home/project$ ./greet.sh
Enter your name :Huyen
Welcome Huyen
Congratulations! You just created and ran your first shell script using Bash on IBM Skills Network
theia@theia-many37758:/home/project$ ls -l greetnew.sh
-rw-r--r-- 1 theia users 0 Sep 12 00:09 greetnew.sh
theia@theia-many37758:/home/project$ firstname = Huyen
bash: firstname: command not found
theia@theia-many37758:/home/project$ chmode u+x greetnew.sh
bash: chmode: command not found
theia@theia-many37758:/home/project$ chmod u+x greetnew.sh
theia@theia-many37758:/home/project$ ./greetnew.sh
Enter your firstname :huyen
Enter your lastname :khanh 
Hello huyen khanh.
theia@theia-many37758:/home/project$ 

theia@theia-many37758:/home/project$ echo '#!/bin/bash' > script.sh
theia@theia-many37758:/home/project$ chmod u+x script.sh
theia@theia-many37758:/home/project$ ./script.sh
Are you enjoying this course so far?
Enter "y" for yes, "n" for no.y
theia@theia-many37758:/home/project$ ./script.sh
Do you like me?
Enter "y" for yes, "n" for no.y
./script.sh: line 7: [y: command not found
./script.sh: line 10: [y: command not found
Your response must be either 'y' or 'n'.
theia@theia-many37758:/home/project$ ./script.sh
Do you like me?
Enter "y" for yes, "n" for no.n
oke, me too
theia@theia-many37758:/home/project$ ./script.sh
Do you like me?
Enter "y" for yes, "n" for no.y
I like you too
theia@theia-many37758:/home/project$ 
theia@theia-many37758:/home/project$ echo '#!/bin/bash' > total.sh
theia@theia-many37758:/home/project$ chmod u+x total.sh
theia@theia-many37758:/home/project$ ./total.sh
theia@theia-many37758:/home/project$ ./total.sh
 Enter num 1: 11
 Enter num 2: 4
The sum of 11 and 4 is 15
The product of 11 and 4 is 44
theia@theia-many37758:/home/project$ ./total.sh
 Enter num 1: 11
 Enter num 2: 4
The sum of 11 and 4 is 15
The product of 11 and 4 is 44
theia@theia-many37758:/home/project$ ./total.sh
 Enter num 1: 11
 Enter num 2: 4
The sum of 11 and 4 is 15
The product of 11 and 4 is 44
The sum is less than the product.
theia@theia-many37758:/home/project$ 
theia@theia-many37758:/home/project$ csv_file="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/M3/L2/arrays_table.csv"
theia@theia-many37758:/home/project$ wget $csv_file
--2023-09-12 13:00:36--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/M3/L2/arrays_table.csv
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54 [text/csv]
Saving to: ‘arrays_table.csv’

arrays_table.csv        100%[===============================>]      54  --.-KB/s    in 0s      

2023-09-12 13:00:36 (10.7 MB/s) - ‘arrays_table.csv’ saved [54/54]

theia@theia-many37758:/home/project$ cat arrays_table.csv
column_0,column_1,column_2
1,2,3
4,5,6
7,8,9
10,11,12
theia@theia-many37758:/home/project$ echo "#!/bin/bash" > array.sh
bash: !/bin/bash: event not found
theia@theia-many37758:/home/project$ echo '#!/bin/bash' > array.sh
theia@theia-many37758:/home/project$ chmod u+x array.sh
theia@theia-many37758:/home/project$ ./array.sh
Displaying the first column:
column_0 1 4 7 10
theia@theia-many37758:/home/project$ ./array.sh
Displaying the first column:
column_0 1 4 7 10
There are 5 lines in the file
column_3 1 1 1 1
theia@theia-many37758:/home/project$ ls
array.sh  arrays_table.csv  conditional_script.sh  script.sh  total.sh
theia@theia-many37758:/home/project$ ./array.sh
Displaying the first column:
column_0 1 4 7 10
There are 5 lines in the file
column_3 1 1 1 1
theia@theia-many37758:/home/project$ ls
array.sh          column_3.txt           report.csv  total.sh
arrays_table.csv  conditional_script.sh  script.sh
theia@theia-many37758:/home/project$ 

CRONTAB
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