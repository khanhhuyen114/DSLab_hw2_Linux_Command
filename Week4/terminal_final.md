theia@theiadocker-many37758:/home/project$ ./backup.sh
bash: ./backup.sh: Permission denied
theia@theiadocker-many37758:/home/project$ chmod u+x backup.sh
theia@theiadocker-many37758:/home/project$ ./backup.sh
backup.sh target_directory_name destination_directory_name
theia@theiadocker-many37758:/home/project$ ls -l backup.sh
-rwxr--r-- 1 theia users 1434 Sep 14 14:00 backup.sh
theia@theiadocker-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/important-documents.zip
--2023-09-14 14:03:41--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/important-documents.zip
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4995 (4.9K) [application/zip]
Saving to: ‘important-documents.zip’

important-documents. 100%[===================>]   4.88K  --.-KB/s    in 0s      

2023-09-14 14:03:41 (827 MB/s) - ‘important-documents.zip’ saved [4995/4995]

theia@theiadocker-many37758:/home/project$ unzip -DDo important-documents.zip
Archive:  important-documents.zip
   creating: important-documents/
  inflating: important-documents/zop.txt  
  inflating: important-documents/ana.txt  
  inflating: important-documents/doi.txt  
theia@theiadocker-many37758:/home/project$ touch important-documents/*
theia@theiadocker-many37758:/home/project$ ./backup.sh important-documents .
The value of targetDirectory is important-documents
The value of destinationDirectory is .
date: extra operand ‘%s’
Try 'date --help' for more information.
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
tar: Cowardly refusing to create an empty archive
Try 'tar --help' or 'tar --usage' for more information.
mv: cannot stat 'backup-[].tar.gz': No such file or directory
theia@theiadocker-many37758:/home/project$ chmod u+x backup.sh
theia@theiadocker-many37758:/home/project$ ls -l backup.sj
ls: cannot access 'backup.sj': No such file or directory
theia@theiadocker-many37758:/home/project$ ls -l backup.sh
-rwxr--r-- 1 theia users 1433 Sep 14 14:06 backup.sh
theia@theiadocker-many37758:/home/project$ ./backup.sh important-documents .
The value of targetDirectory is important-documents
The value of destinationDirectory is .
./backup.sh: line 27: 1694714890: command not found
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
date: extra operand ‘%s’
Try 'date --help' for more information.
./backup.sh: line 58: ((: > -86400: syntax error: operand expected (error token is "> -86400")
tar: Cowardly refusing to create an empty archive
Try 'tar --help' or 'tar --usage' for more information.
mv: cannot stat 'backup-[].tar.gz': No such file or directory
theia@theiadocker-many37758:/home/project$ ./backup.sh important-documents .
The value of targetDirectory is important-documents
The value of destinationDirectory is .
./backup.sh: line 27: 1694714945: command not found



ana.txt
doi.txt
zop.txt
theia@theiadocker-many37758:/home/project$ ./backup.sh important-documents .
The value of targetDirectory is important-documents
The value of destinationDirectory is .



ana.txt
doi.txt
zop.txt
theia@theiadocker-many37758:/home/project$ ls -l
total 32
-rw-r--r-- 1 theia users 4419 Sep 14 14:09 'backup-[1694714969].tar.gz'
-rwxr--r-- 1 theia users 1430 Sep 14 14:09  backup.sh
-rw-r--r-- 1 theia users 4419 Sep 14 14:09 'backup-[].tar.gz'
drwxr-sr-x 2 theia users 4096 Sep 14 14:09  important-documents
-rw-r--r-- 1 theia users 4995 Sep 28  2022  important-documents.zip
theia@theiadocker-many37758:/home/project$ crontab -e
no crontab for theia - using an empty one
crontab: installing new crontab
theia@theiadocker-many37758:/home/project$ sudo service cron start
 * Starting periodic command scheduler cron
   ...done.
theia@theiadocker-many37758:/home/project$ ls -l
total 32
-rw-r--r-- 1 theia users 4419 Sep 14 14:09 'backup-[1694714969].tar.gz'
-rwxr--r-- 1 theia users 1430 Sep 14 14:09  backup.sh
-rw-r--r-- 1 theia users 4419 Sep 14 14:09 'backup-[].tar.gz'
drwxr-sr-x 2 theia users 4096 Sep 14 14:09  important-documents
-rw-r--r-- 1 theia users 4995 Sep 28  2022  important-documents.zip
theia@theiadocker-many37758:/home/project$ crontab -l
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
theia@theiadocker-many37758:/home/project$ 







