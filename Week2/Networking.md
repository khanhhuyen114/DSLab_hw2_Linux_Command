theia@theia-many37758:/home/project$ hostname
theia-many37758
theia@theia-many37758:/home/project$ hostname -i
172.22.170.168
theia@theia-many37758:/home/project$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1480
        inet 172.22.170.168  netmask 255.255.255.255  broadcast 0.0.0.0
        inet6 fe80::8c6e:b5ff:fed9:a65b  prefixlen 64  scopeid 0x20<link>
        ether 8e:6e:b5:d9:a6:5b  txqueuelen 0  (Ethernet)
        RX packets 17891  bytes 9254654 (9.2 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 16005  bytes 36896679 (36.8 MB)
        TX errors 0  dropped 1 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 42217  bytes 79785603 (79.7 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 42217  bytes 79785603 (79.7 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

theia@theia-many37758:/home/project$ ifconfig eth0
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1480
        inet 172.22.170.168  netmask 255.255.255.255  broadcast 0.0.0.0
        inet6 fe80::8c6e:b5ff:fed9:a65b  prefixlen 64  scopeid 0x20<link>
        ether 8e:6e:b5:d9:a6:5b  txqueuelen 0  (Ethernet)
        RX packets 18115  bytes 9297502 (9.2 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 16201  bytes 36936254 (36.9 MB)
        TX errors 0  dropped 1 overruns 0  carrier 0  collisions 0

theia@theia-many37758:/home/project$ ping www.google.com
PING www.google.com (172.253.63.105): 56 data bytes
64 bytes from 172.253.63.105: icmp_seq=0 ttl=105 time=1.259 ms
64 bytes from 172.253.63.105: icmp_seq=1 ttl=105 time=1.391 ms
64 bytes from 172.253.63.105: icmp_seq=2 ttl=105 time=1.391 ms
64 bytes from 172.253.63.105: icmp_seq=3 ttl=105 time=1.471 ms
64 bytes from 172.253.63.105: icmp_seq=4 ttl=105 time=1.557 ms
^C--- www.google.com ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
round-trip min/avg/max/stddev = 1.259/1.414/1.557/0.099 ms
theia@theia-many37758:/home/project$ ping -c 5 www.google.com
PING www.google.com (172.253.63.147): 56 data bytes
64 bytes from 172.253.63.147: icmp_seq=0 ttl=105 time=1.221 ms
64 bytes from 172.253.63.147: icmp_seq=1 ttl=105 time=1.477 ms
64 bytes from 172.253.63.147: icmp_seq=2 ttl=105 time=1.395 ms
64 bytes from 172.253.63.147: icmp_seq=3 ttl=105 time=1.252 ms
64 bytes from 172.253.63.147: icmp_seq=4 ttl=105 time=1.379 ms
--- www.google.com ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
round-trip min/avg/max/stddev = 1.221/1.345/1.477/0.095 ms
theia@theia-many37758:/home/project$ curl https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/usdoi.txt
The unanimous Declaration of the thirteen united States of America, When in the
Course of human events, it becomes necessary for one people to dissolve the
political bands which have connected them with another, and to assume among the
powers of the earth, the separate and equal station to which the Laws of Nature
...
theia@theia-many37758:/home/project$ rm usdoi.txt
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/usdoi.txt
--2023-09-15 23:50:07--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/usdoi.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8121 (7.9K) [text/plain]
Saving to: ‘usdoi.txt’

usdoi.txt               100%[===============================>]   7.93K  --.-KB/s    in 0s      

2023-09-15 23:50:07 (1.21 GB/s) - ‘usdoi.txt’ saved [8121/8121]

theia@theia-many37758:/home/project$ cd `/home/project`
bash: /home/project: Is a directory
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ host
bash: host: command not found
theia@theia-many37758:~$ cd home/project
bash: cd: home/project: No such file or directory
theia@theia-many37758:~$ cd `/home/project`
bash: /home/project: Is a directory
theia@theia-many37758:~$ cd
theia@theia-many37758:~$ cd /
theia@theia-many37758:/$ cd .
theia@theia-many37758:/$ cd project
bash: cd: project: No such file or directory
theia@theia-many37758:/$ pwd
/
theia@theia-many37758:/$ cd home/project
theia@theia-many37758:/home/project$ host -i
bash: host: command not found
theia@theia-many37758:/home/project$ hostname -i
172.22.170.168
theia@theia-many37758:/home/project$ ping www.google.com
PING www.google.com (172.253.122.106): 56 data bytes
64 bytes from 172.253.122.106: icmp_seq=0 ttl=105 time=1.702 ms
64 bytes from 172.253.122.106: icmp_seq=1 ttl=105 time=1.844 ms
64 bytes from 172.253.122.106: icmp_seq=2 ttl=105 time=1.800 ms
64 bytes from 172.253.122.106: icmp_seq=3 ttl=105 time=1.857 ms
^C--- www.google.com ping statistics ---
4 packets transmitted, 4 packets received, 0% packet loss
round-trip min/avg/max/stddev = 1.702/1.801/1.857/0.061 ms
theia@theia-many37758:/home/project$ ifconfig eth0
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1480
        inet 172.22.170.168  netmask 255.255.255.255  broadcast 0.0.0.0
        inet6 fe80::8c6e:b5ff:fed9:a65b  prefixlen 64  scopeid 0x20<link>
        ether 8e:6e:b5:d9:a6:5b  txqueuelen 0  (Ethernet)
        RX packets 21679  bytes 10013215 (10.0 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 19303  bytes 37627659 (37.6 MB)
        TX errors 0  dropped 1 overruns 0  carrier 0  collisions 0

theia@theia-many37758:/home/project$ curl www.google.com
<!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="en"><head><meta content="Search the world's information, including webpages, images, videos and more. Google has many special features to help you find exactly what you're looking for." name="description"><meta content="noodp" name="robots"><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/logos/doodles/2023/project$ wget www.google.com
...
--2023-09-15 23:54:33--  http://www.google.com/
Resolving www.google.com (www.google.com)... 172.253.122.147, 172.253.122.104, 172.253.122.106, ...
Connecting to www.google.com (www.google.com)|172.253.122.147|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: ‘index.html’

index.html                  [ <=>                            ]  19.96K  --.-KB/s    in 0.001s  

2023-09-15 23:54:33 (36.1 MB/s) - ‘index.html’ saved [20437]

theia@theia-many37758:/home/project$ ls -l
total 40
-rw-r--r-- 1 theia users 20437 Sep 15 23:54 index.html
-rw-r--r-- 1 theia users    42 May 15 14:56 names_and_numbers.csv
-rw-r--r-- 1 theia users  8121 Sep 21  2022 usdoi.txt
-rw-r--r-- 1 theia users    20 Sep 28  2022 zoo_ages.txt
-rw-r--r-- 1 theia users    54 Sep 28  2022 zoo.txt
theia@theia-many37758:/home/project$ 