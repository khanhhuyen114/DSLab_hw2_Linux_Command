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