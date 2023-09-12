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