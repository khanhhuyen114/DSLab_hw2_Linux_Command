theia@theia-many37758:/home/project$ tar -cvf bin.tar /bin
tar: Removing leading `/' from member names
/bin/
/bin/zdiff
/bin/su
/bin/more
/bin/mountpoint
/bin/uname
/bin/uncompress
/bin/which
/bin/gzip
/bin/domainname
/bin/run-parts
...

/bin/lessecho
theia@theia-many37758:/home/project$ tar -tvf bin.tar
drwxr-xr-x root/root         0 2023-02-27 12:29 bin/
-rwxr-xr-x root/root      5782 2022-04-08 07:12 bin/zdiff
-rwsr-xr-x root/root     44664 2022-11-29 07:25 bin/su
-rwxr-xr-x root/root     38952 2020-09-16 14:43 bin/more
-rwxr-xr-x root/root     14408 2020-09-16 14:43 bin/mountpoint
-rwxr-xr-x root/root     35032 2018-01-18 04:43 bin/uname
-rwxr-xr-x root/root      2301 2022-04-08 07:12 bin/uncompress
-rwxr-xr-x root/root       946 2017-12-30 13:15 bin/which
...

theia@theia-many37758:/home/project$ tar -xvf bin.tar
bin/
bin/zdiff
bin/su
bin/more
bin/mountpoint
bin/uname
bin/uncompress
bin/which
bin/gzip
bin/domainname
bin/run-parts
...
theia@theia-many37758:/home/project$ ls -l
total 5616
drwxr-sr-x 2 theia users    4096 Feb 27  2023 bin
-rw-r--r-- 1 theia users 5703680 Sep 16 00:02 bin.tar
-rw-r--r-- 1 theia users   20437 Sep 15 23:54 index.html
-rw-r--r-- 1 theia users      42 May 15 14:56 names_and_numbers.csv
-rw-r--r-- 1 theia users    8121 Sep 21  2022 usdoi.txt
-rw-r--r-- 1 theia users      20 Sep 28  2022 zoo_ages.txt
-rw-r--r-- 1 theia users      54 Sep 28  2022 zoo.txt
theia@theia-many37758:/home/project$ zip config.zip /etc/*.conf
  adding: etc/adduser.conf (deflated 55%)
  adding: etc/ca-certificates.conf (deflated 74%)
  adding: etc/debconf.conf (deflated 56%)
  adding: etc/deluser.conf (deflated 40%)
  adding: etc/gai.conf (deflated 57%)
  ...
theia@theia-many37758:/home/project$ zip -r bin.zip /bin
  adding: bin/ (stored 0%)
  adding: bin/zdiff (deflated 66%)
  adding: bin/su (deflated 61%)
  adding: bin/more (deflated 52%)
  adding: bin/mountpoint (deflated 68%)
  adding: bin/uname (deflated 58%)
  adding: bin/uncompress (deflated 50%)
  ...
theia@theia-many37758:/home/project$ unzip -l config.zip
Archive:  config.zip
  Length      Date    Time    Name
---------  ---------- -----   ----
     3028  2023-01-26 03:31   etc/adduser.conf
     5432  2023-02-27 12:12   etc/ca-certificates.conf
     2969  2018-02-28 04:50   etc/debconf.conf
      604  2017-08-13 14:17   etc/deluser.conf
     2584  2018-02-01 11:17   etc/gai.conf
       92  2018-04-09 07:10   etc/host.conf
       34  2016-01-27 09:17   etc/ld.so.conf
      191  2018-02-07 18:59   etc/libaudit.conf
      703  2017-08-21 13:38   etc/logrotate.conf
      812  2018-03-24 15:13   etc/mke2fs.conf
     2154  2019-03-22 09:34   etc/mongodb.conf
      497  2016-10-05 15:57   etc/nsswitch.conf
     2517  2020-08-17 21:58   etc/ntp.conf
      552  2018-04-04 17:56   etc/pam.conf
      115  2023-09-15 22:58   etc/resolv.conf
    10368  2022-03-31 16:53   etc/sensors3.conf
     2683  2018-01-17 17:35   etc/sysctl.conf
     1260  2018-02-25 19:58   etc/ucf.conf
---------                     -------
    36595                     18 files
theia@theia-many37758:/home/project$ unzip -o bin.zip
Archive:  bin.zip
  inflating: bin/zdiff               
  inflating: bin/su                  
  inflating: bin/more                
  inflating: bin/mountpoint          
  inflating: bin/uname               
  inflating: bin/uncompress          
  inflating: bin/which               
  inflating: bin/gzip                
  ...    
theia@theia-many37758:/home/project$ 