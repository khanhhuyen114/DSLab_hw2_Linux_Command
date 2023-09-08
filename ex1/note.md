theia@theia-many37758:/home/project$ ls
theia@theia-many37758:/home/project$ ls/
bash: ls/: No such file or directory
theia@theia-many37758:/home/project$ ls /
bin   dev  home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  etc  lib   lib64  media   opt  root  sbin  sys  usr
theia@theia-many37758:/home/project$ ls /bin
bash          chgrp          false     lesspipe    nisdomainname  sh.distrib  which
bunzip2       chmod          fgrep     ln          pidof          sleep       ypdomainname
bzcat         chown          findmnt   login       ping           stty        zcat
bzcmp         cp             fuser     ls          ping6          su          zcmp
bzdiff        dash           grep      lsblk       ps             sync        zdiff
bzegrep       date           gunzip    mkdir       pwd            tar         zegrep
bzexe         dd             gzexe     mknod       rbash          tempfile    zfgrep
bzfgrep       df             gzip      mktemp      readlink       touch       zforce
bzgrep        dir            hostname  more        rm             true        zgrep
bzip2         dmesg          kill      mount       rmdir          umount      zless
bzip2recover  dnsdomainname  less      mountpoint  rnano          uname       zmore
bzless        domainname     lessecho  mv          run-parts      uncompress  znew
bzmore        echo           lessfile  nano        sed            vdir
cat           egrep          lesskey   netstat     sh             wdctl
theia@theia-many37758:/home/project$ /bin/ls
theia@theia-many37758:/home/project$ ls /bin/ls
/bin/ls
theia@theia-many37758:/home/project$ cd ~
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ cd ..
theia@theia-many37758:/home$ cd /
theia@theia-many37758:/$ cd bin
theia@theia-many37758:/bin$ cd ..
theia@theia-many37758:/$ cd ./bin
theia@theia-many37758:/bin$ cd ../home/theia
theia@theia-many37758:~$ cd../project
bash: cd../project: No such file or directory
theia@theia-many37758:~$ cd ../project
theia@theia-many37758:/home/project$ pwd
/home/project
theia@theia-many37758:/home/project$ cd /bin/
theia@theia-many37758:/bin$ 
theia@theia-many37758:/$ ls /home/theia/dsdriver/bin
clpplus  db2cli  db2diag  db2dsdcfgfill  db2ldcfg  db2lddrg  db2level  db2support
theia@theia-many37758:/$ cd ~
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ cd /bin/
theia@theia-many37758:/bin$ cd..
bash: cd..: command not found
theia@theia-many37758:/bin$ cd ..
theia@theia-many37758:/$ /b
bin/  boot/ 
theia@theia-many37758:/$ /bin/
bash: /bin/: Is a directory
theia@theia-many37758:/$ cd /bin/
theia@theia-many37758:/bin$ cd ~
theia@theia-many37758:~$ 
#3
theia@theia-many37758:/home/project$ sudo apt update

theia@theia-many37758:/home/project$ sudo apt upgrade nano
theia@theia-many37758:/home/project$ sudo apt install vim
theia@theia-many37758:/home/project$ ls
theia@theia-many37758:/home/project$ nano hello_world.txt
theia@theia-many37758:/home/project$ LS
bash: LS: command not found
theia@theia-many37758:/home/project$ ls
hello_world.txt
theia@theia-many37758:/home/project$ cat hellp_world.txt
cat: hellp_world.txt: No such file or directory
theia@theia-many37758:/home/project$ cat hello_world.txt
Hello world!
This is the second line of my first-ever text file created with nano.
theia@theia-many37758:/home/project$ vim
theia@theia-many37758:/home/project$ vim hello_world_2.txt
theia@theia-many37758:/home/project$ nano hello_world.txt
theia@theia-many37758:/home/project$ 
theia@theia-many37758:/home/project$ 
theia@theia-many37758:/home/project$ vim done.txt
theia@theia-many37758:/home/project$ bash done.txt
I am done with the lab
theia@theia-many37758:/home/project$