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
...
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
....
theia@theia-many37758:~/tmp$ cp /var/log/bootstrap.log .
theia@theia-many37758:~/tmp$ ls
bootstrap.log