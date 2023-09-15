theia@theia-many37758:/home/project$ whoami
theia
theia@theia-many37758:/home/project$ uname
Linux
theia@theia-many37758:/home/project$ uname -a
Linux theia-many37758 5.4.0-156-generic #173-Ubuntu SMP Tue Jul 11 07:25:22 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux
theia@theia-many37758:/home/project$ id
uid=1000(theia) gid=1000(theia) groups=1000(theia),27(sudo),100(users)
theia@theia-many37758:/home/project$ df
theia@theia-many37758:/home/project$ top
theia@theia-many37758:/home/project$ top -n 10
             
theia@theia-many37758:/home/project$ date
Mon Sep 11 03:13:46 EDT 2023
theia@theia-many37758:/home/project$ date '+%T'
03:14:05
theia@theia-many37758:/home/project$ echo 'Hello!\nGoodbye!'
Hello!\nGoodbye!
theia@theia-many37758:/home/project$ echo -e 'Hello!\nGoodbye!'
Hello!
Goodbye!
theia@theia-many37758:/home/project$ 
theia@theia-many37758:/home/project$ pwd
/home/project
theia@theia-many37758:/home/project$ ls
theia@theia-many37758:/home/project$ ls /bin

theia@theia-many37758:/home/project$ mkdir scripts
theia@theia-many37758:/home/project$ ls
scripts
theia@theia-many37758:/home/project$ cd scripts
theia@theia-many37758:/home/project/scripts$ pwd
/home/project/scripts
theia@theia-many37758:/home/project/scripts$ cd
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ cd ..
theia@theia-many37758:/home$ cd
theia@theia-many37758:~$ touch myfile.txt
theia@theia-many37758:~$ ls
docker-compose         javasharedresources  package.json  skills-network-extension-v0.1.0.tgz
dsdriver               lib                  plugins       src-gen
entrypoint.sh          myfile.txt           postgres      webpack.config.js
gen-webpack.config.js  node_modules         README.md     yarn.lock
theia@theia-many37758:~$ touch myfile.txt
theia@theia-many37758:~$ date -r myfile.txt
Mon Sep 11 03:42:25 EDT 2023
theia@theia-many37758:~$ find /etc -name \'*.txt\'
find: ‘/etc/ssl/private’: Permission denied
theia@theia-many37758:~$ rm -i myfile.txt
rm: remove regular empty file 'myfile.txt'? y
theia@theia-many37758:~$ ls
docker-compose         lib           README.md
dsdriver               node_modules  skills-network-extension-v0.1.0.tgz
entrypoint.sh          package.json  src-gen
gen-webpack.config.js  plugins       webpack.config.js
javasharedresources    postgres      yarn.lock
theia@theia-many37758:~$ touch users.txt
theia@theia-many37758:~$ mv users.txt user-info.txt
theia@theia-many37758:~$ ls
docker-compose         node_modules                         src-gen
dsdriver               package.json                         user-info.txt
entrypoint.sh          plugins                              webpack.config.js
gen-webpack.config.js  postgres                             yarn.lock
javasharedresources    README.md
lib                    skills-network-extension-v0.1.0.tgz
theia@theia-many37758:~$ mv user-info.txt /tmp
theia@theia-many37758:~$ ls
docker-compose         lib           README.md
dsdriver               node_modules  skills-network-extension-v0.1.0.tgz
entrypoint.sh          package.json  src-gen
gen-webpack.config.js  plugins       webpack.config.js
javasharedresources    postgres      yarn.lock
theia@theia-many37758:~$ ls -l /tmp
total 13412
theia@theia-many37758:~$ cp /tmp/user-info.txt user-info.txt
theia@theia-many37758:~$ ls
docker-compose         node_modules                         src-gen
dsdriver               package.json                         user-info.txt
entrypoint.sh          plugins                              webpack.config.js
gen-webpack.config.js  postgres                             yarn.lock
javasharedresources    README.md
lib                    skills-network-extension-v0.1.0.tgz
theia@theia-many37758:~$ cp /etc/passwd users.txt
theia@theia-many37758:~$ ls
docker-compose         lib           README.md                            webpack.config.js
dsdriver               node_modules  skills-network-extension-v0.1.0.tgz  yarn.lock
entrypoint.sh          package.json  src-gen
gen-webpack.config.js  plugins       user-info.txt
javasharedresources    postgres      users.txt
theia@theia-many37758:~$ ls /home
project  theia
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ cd
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ mkdir tmp
theia@theia-many37758:~$ ls
docker-compose         lib           README.md                            users.txt
dsdriver               node_modules  skills-network-extension-v0.1.0.tgz  webpack.config.js
entrypoint.sh          package.json  src-gen                              yarn.lock
gen-webpack.config.js  plugins       tmp
javasharedresources    postgres      user-info.txt
theia@theia-many37758:~$ cd tmp
theia@theia-many37758:~/tmp$ touch display.sh
theia@theia-many37758:~/tmp$ ls
display.sh
theia@theia-many37758:~/tmp$ cp display.sh report.sh
theia@theia-many37758:~/tmp$ rm report.sh ../
rm: cannot remove '../': Is a directory
theia@theia-many37758:~/tmp$ mv report.sh ../
mv: cannot stat 'report.sh': No such file or directory
theia@theia-many37758:~/tmp$ ls
display.sh
theia@theia-many37758:~/tmp$ cp display.sh report.sh
theia@theia-many37758:~/tmp$ ls
display.sh  report.sh
theia@theia-many37758:~/tmp$ mv report.sh ../
theia@theia-many37758:~/tmp$ ls ../
docker-compose         lib           README.md                            user-info.txt
dsdriver               node_modules  report.sh                            users.txt
entrypoint.sh          package.json  skills-network-extension-v0.1.0.tgz  webpack.config.js
gen-webpack.config.js  plugins       src-gen                              yarn.lock
javasharedresources    postgres      tmp
theia@theia-many37758:~/tmp$ rm display.sh
theia@theia-many37758:~/tmp$ ls
theia@theia-many37758:~/tmp$ ls -ltr /etc/
total 668
-rw-r--r-- 1 root     root        34 Jan 27  2016 ld.so.conf
-rw-r--r-- 1 root     root       367 Jan 27  2016 bindresvport.blacklist
-rw-r--r-- 1 root     root     24301 Jul 15  2016 mime.types
-rw-r--r-- 1 root     root       449 Jul 15  2016 mailcap.order
-rw-r--r-- 1 root     root       497 Oct  5  2016 nsswitch.conf
-rw-r--r-- 1 root     root     19183 Dec 25  2016 services
-rw-r--r-- 1 root     root       887 Dec 25  2016 rpc
-rw-r--r-- 1 root     root      2932 Dec 25  2016 protocols
drwxr-xr-x 2 root     root      4096 Dec 25  2016 network
-rw-r--r-- 1 root     root      1748 May 15  2017 inputrc
-rw-r--r-- 1 root     root        11 Jun 25  2017 debian_version
-rwxr-xr-x 1 root     root       268 Jul 21  2017 rmt
-rw-r--r-- 1 root     root       604 Aug 13  2017 deluser.conf
-rw-r--r-- 1 root     root       703 Aug 21  2017 logrotate.conf
drwxr-xr-x 1 root     root      4096 Oct 25  2017 systemd
-rw-r--r-- 1 root     root      2683 Jan 17  2018 sysctl.conf
-rw-r--r-- 1 root     root      4141 Jan 25  2018 securetty
-rw-r--r-- 1 root     root     10550 Jan 25  2018 login.defs
-rw-r--r-- 1 root     root      2584 Feb  1  2018 gai.conf
-rw-r--r-- 1 root     root       191 Feb  7  2018 libaudit.conf
-rw-r--r-- 1 root     root      9048 Feb 13  2018 nanorc
-rw-r--r-- 1 root     root      1260 Feb 25  2018 ucf.conf
-rw-r--r-- 1 root     root      2969 Feb 28  2018 debconf.conf
-rw-r--r-- 1 root     root       812 Mar 24  2018 mke2fs.conf
-rw-r--r-- 1 root     root       552 Apr  4  2018 pam.conf
-rw-r--r-- 1 root     root        91 Apr  9  2018 networks
-rw-r--r-- 1 root     root       267 Apr  9  2018 legal
-rw-r--r-- 1 root     root        92 Apr  9  2018 host.conf
-rw-r--r-- 1 root     root      5174 Aug  4  2018 manpath.config
-rw-r--r-- 1 root     root      2154 Mar 22  2019 mongodb.conf
-rw-r--r-- 1 root     root      4942 Apr  8  2019 wgetrc
-rw-r--r-- 1 root     root       111 May 12  2020 magic.mime
-rw-r--r-- 1 root     root       111 May 12  2020 magic
-rw-r--r-- 1 root     root      2517 Aug 17  2020 ntp.conf
lrwxrwxrwx 1 root     root        21 Sep  6  2021 os-release -> ../usr/lib/os-release
-rw-r--r-- 1 root     root       105 Sep  6  2021 lsb-release
-rw-r--r-- 1 root     root        19 Sep  6  2021 issue.net
-rw-r--r-- 1 root     root        26 Sep  6  2021 issue
drwxr-xr-x 2 root     root      4096 Oct 21  2021 docker
-rw-r--r-- 1 root     root     10368 Mar 31  2022 sensors3.conf
-rw-r--r-- 1 root     root      2995 May  3  2022 locale.alias
-rw-r--r-- 1 root     root       722 May 10  2022 crontab
drwxr-xr-x 2 root     root      4096 Jan 26  2023 opt
-rw-r--r-- 1 root     root        37 Jan 26  2023 fstab
-rw-r--r-- 1 root     root        73 Jan 26  2023 shells
-rw-r--r-- 1 root     root         0 Jan 26  2023 subuid-
-rw-r--r-- 1 root     root         0 Jan 26  2023 subgid-
drwxr-xr-x 1 root     root      4096 Jan 26  2023 kernel
-rw-r--r-- 1 root     root      3028 Jan 26  2023 adduser.conf
drwxr-xr-x 2 root     root      4096 Jan 26  2023 selinux
drwxr-xr-x 2 root     root      4096 Jan 26  2023 skel
drwxr-xr-x 2 root     root      4096 Jan 26  2023 terminfo
drwxr-xr-x 1 root     root      4096 Jan 26  2023 security
-rw-r--r-- 1 root     root       106 Jan 26  2023 environment
-rw-r--r-- 1 root     root         0 Jan 26  2023 machine-id
drwxr-xr-x 2 root     root      4096 Jan 26  2023 cloud
drwxr-xr-x 2 root     root      4096 Feb 27  2023 python3.6
drwxr-xr-x 2 root     root      4096 Feb 27  2023 python2.7
drwxr-xr-x 4 root     root      4096 Feb 27  2023 perl
drwxr-xr-x 3 root     root      4096 Feb 27  2023 ca-certificates
drwxr-xr-x 4 root     root      4096 Feb 27  2023 dbus-1
drwxr-xr-x 3 root     root      4096 Feb 27  2023 gss
drwxr-xr-x 3 root     root      4096 Feb 27  2023 logcheck
drwxr-xr-x 3 root     root      4096 Feb 27  2023 xml
drwxr-xr-x 3 root     root      4096 Feb 27  2023 java
drwxr-xr-x 2 root     root      4096 Feb 27  2023 sudoers.d
drwxr-xr-x 3 root     root      4096 Feb 27  2023 pm
drwxr-xr-x 2 root     root      4096 Feb 27  2023 ldap
drwxr-xr-x 1 root     root      4096 Feb 27  2023 ssl
drwxr-xr-x 4 root     root      4096 Feb 27  2023 lighttpd
drwxr-xr-x 1 root     root      4096 Feb 27  2023 pam.d
drwxr-xr-x 2 root     root      4096 Feb 27  2023 cron.monthly
drwxr-xr-x 2 root     root      4096 Feb 27  2023 cron.hourly
-rw-r--r-- 1 root     root      5432 Feb 27  2023 ca-certificates.conf
drwxr-xr-x 3 root     root      4096 Feb 27  2023 xdg
drwxr-xr-x 4 root     root      4096 Feb 27  2023 fonts
drwxr-xr-x 2 root     root      4096 Feb 27  2023 python3
drwxr-xr-x 2 root     root      4096 Feb 27  2023 python
drwxr-xr-x 2 root     root      4096 Feb 27  2023 ssh
drwxr-xr-x 1 root     root      4096 Feb 27  2023 update-motd.d
drwxr-xr-x 5 root     root      4096 Feb 27  2023 java-11-openjdk
drwxr-xr-x 1 root     root      4096 Feb 27  2023 dpkg
drwxr-xr-x 2 root     root      4096 Feb 27  2023 bash_completion.d
drwxr-xr-x 2 root     root      4096 Feb 27  2023 groovy
-r--r----- 1 root     root       784 Feb 27  2023 sudoers
-rw-r--r-- 1 root     root        19 Feb 27  2023 subuid
-rw-r--r-- 1 root     root        19 Feb 27  2023 subgid
drwxr-xr-x 1 root     root      4096 Feb 27  2023 ld.so.conf.d
drwxr-xr-x 3 root     root      4096 Feb 27  2023 gdb
drwxr-xr-x 2 root     root      4096 Feb 27  2023 python3.8
drwxr-xr-x 3 root     root      4096 Feb 27  2023 ufw
drwxr-xr-x 1 root     root      4096 Feb 27  2023 php
-rw-r--r-- 1 root     root        17 Feb 27  2023 timezone
lrwxrwxrwx 1 root     root        36 Feb 27  2023 localtime -> /usr/share/zoneinfo/America/New_York
drwxr-xr-x 2 root     root      4096 Feb 27  2023 groff
drwxr-xr-x 2 root     root      4096 Feb 27  2023 calendar
-rw-r--r-- 1 root     root      9397 Feb 27  2023 locale.gen
drwxr-xr-x 1 root     root      4096 Feb 27  2023 cron.weekly
-rw-r--r-- 1 root     root      2621 Feb 27  2023 mailcap
-rw-r--r-- 1 root     root       581 Feb 27  2023 profile
-rw-r--r-- 1 root     root      2319 Feb 27  2023 bash.bashrc
drwxr-xr-x 3 root     root      4096 Feb 27  2023 NetworkManager
drwxr-xr-x 3 root     root      4096 Feb 27  2023 dhcp
drwxr-xr-x 3 root     root      4096 Feb 27  2023 apparmor
drwxr-xr-x 1 root     root      4096 Feb 27  2023 X11
drwxr-xr-x 1 root     root      4096 Feb 27  2023 sysctl.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rcS.d
drwxr-xr-x 5 root     root      4096 Feb 27  2023 java-8-openjdk
drwxr-xr-x 3 root     root      4096 Feb 27  2023 cassandra
drwxr-xr-x 1 root     root      4096 Feb 27  2023 apparmor.d
drwxr-xr-x 2 root     root      4096 Feb 27  2023 sysstat
drwxr-xr-x 2 root     root      4096 Feb 27  2023 sensors.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 profile.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 default
drwxr-xr-x 1 root     root      4096 Feb 27  2023 cron.daily
drwxr-xr-x 1 root     root      4096 Feb 27  2023 cron.d
-rw-r----- 1 root     shadow     675 Feb 27  2023 shadow-
-rw-r----- 1 root     shadow     675 Feb 27  2023 shadow
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc6.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc5.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc4.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc3.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc2.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc1.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 rc0.d
drwxr-xr-x 3 root     root      4096 Feb 27  2023 postgresql-common
drwxr-xr-x 3 postgres postgres  4096 Feb 27  2023 postgresql
-rw-r--r-- 1 root     root      1252 Feb 27  2023 passwd-
-rw-r--r-- 1 root     root      1279 Feb 27  2023 passwd
drwxr-xr-x 1 root     root      4096 Feb 27  2023 logrotate.d
drwxr-xr-x 1 root     root      4096 Feb 27  2023 init.d
-rw-r----- 1 root     shadow     495 Feb 27  2023 gshadow-
-rw-r----- 1 root     shadow     503 Feb 27  2023 gshadow
-rw-r--r-- 1 root     root       598 Feb 27  2023 group-
-rw-r--r-- 1 root     root       606 Feb 27  2023 group
-rw-r--r-- 1 root     root     38873 Feb 27  2023 ld.so.cache
drwxr-xr-x 3 root     root      4096 Feb 27  2023 emacs
drwxr-xr-x 1 root     root      4096 Feb 27  2023 alternatives
drwxr-xr-x 1 root     root      4096 Feb 27  2023 apt
-rw-r--r-- 1 root     root       115 Sep 11 02:58 resolv.conf
-rw-r--r-- 1 root     root        16 Sep 11 02:58 hostname
-rw-r--r-- 1 root     root       262 Sep 11 03:01 hosts
theia@theia-many37758:~/tmp$ cp /var/log/bootstrap.log .
theia@theia-many37758:~/tmp$ ls
bootstrap.log
theia@theia-many37758:~/tmp$ ^C
theia@theia-many37758:~/tmp$ 
theia@theia-many37758:/home/project$ cd /home/project
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/usdoi.txt
--2023-09-11 03:56:13--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/usdoi.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8121 (7.9K) [text/plain]
Saving to: ‘usdoi.txt’

usdoi.txt               100%[===============================>]   7.93K  --.-KB/s    in 0s      

2023-09-11 03:56:13 (734 MB/s) - ‘usdoi.txt’ saved [8121/8121]

theia@theia-many37758:/home/project$ ls -l usdoi.txt
-rw-r--r-- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ chmod -r usdoi.txt
theia@theia-many37758:/home/project$ ls -l usdoi.txt
--w------- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ chmod +r usdoi.txt
theia@theia-many37758:/home/project$ ls -l usdoi.tx
ls: cannot access 'usdoi.tx': No such file or directory
theia@theia-many37758:/home/project$ ls -l usdoi.txt
-rw-r--r-- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ chmod o-r usdoi.txt
theia@theia-many37758:/home/project$ ls -l usdoi.txt
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ mkdir test
theia@theia-many37758:/home/project$ ls -l
total 16
drwxr-sr-x 2 theia users 4096 Sep 11 03:39 scripts
drwxr-sr-x 2 theia users 4096 Sep 11 04:00 test
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ cd test
theia@theia-many37758:/home/project/test$ mkdir test2
theia@theia-many37758:/home/project/test$ cd ../
theia@theia-many37758:/home/project$ chmod -u-x test
theia@theia-many37758:/home/project$ cd test
bash: cd: test: Permission denied
theia@theia-many37758:/home/project$ ls -l
total 16
drwxr-sr-x 2 theia users 4096 Sep 11 03:39 scripts
d-----S--- 3 theia users 4096 Sep 11 04:01 test
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ mkdir test/test3
mkdir: cannot create directory ‘test/test3’: Permission denied
theia@theia-many37758:/home/project$ chmod u+x test
theia@theia-many37758:/home/project$ chmod u-w test
theia@theia-many37758:/home/project$ ls -l
total 16
drwxr-sr-x 2 theia users 4096 Sep 11 03:39 scripts
d--x--S--- 3 theia users 4096 Sep 11 04:01 test
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ cd test
theia@theia-many37758:/home/project/test$ mkdir test_again
mkdir: cannot create directory ‘test_again’: Permission denied
theia@theia-many37758:/home/project/test$ cd ..
theia@theia-many37758:/home/project$ ls -l usdoi.txt
-rw-r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ chmod u-w usdoi.txt
theia@theia-many37758:/home/project$ ls -l usdoi.txt
-r--r----- 1 theia users 8121 Sep 28  2022 usdoi.txt
theia@theia-many37758:/home/project$ rm usdoi.txt
rm: remove write-protected regular file 'usdoi.txt'? y
theia@theia-many37758:/home/project$ ls usdoi.txt
ls: cannot access 'usdoi.txt': No such file or directory
theia@theia-many37758:/home/project$ cd ..
theia@theia-many37758:/home$ mkdir tmp_dir
mkdir: cannot create directory ‘tmp_dir’: Permission denied
theia@theia-many37758:/home$ cd project
theia@theia-many37758:/home/project$ mkdir tmp_dir
theia@theia-many37758:/home/project$ ls -l tmp_dir
total 0
theia@theia-many37758:/home/project$ chmod u-w tmp_dir
theia@theia-many37758:/home/project$ cd tmp_dir
theia@theia-many37758:/home/project/tmp_dir$ mkdir sub_dir
mkdir: cannot create directory ‘sub_dir’: Permission denied
theia@theia-many37758:/home/project/tmp_dir$ 