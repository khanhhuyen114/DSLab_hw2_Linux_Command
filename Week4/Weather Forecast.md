theia@theia-many37758:/home/project$ touch rx_poc1.log
theia@theia-many37758:/home/project$ header=$(echo -e "year\tmonth\tday\tobs_tmp\tfc_temp")
theia@theia-many37758:/home/project$ echo $header>rx_poc1.log
theia@theia-many37758:/home/project$ echo '#!/bin/bash' > rx_poc1.sh
theia@theia-many37758:/home/project$ chmod u+x rx_poc1.sh
theia@theia-many37758:/home/project$ date
Thu Sep 14 06:22:00 EDT 2023
theia@theia-many37758:/home/project$ date -u
Thu Sep 14 10:22:05 UTC 2023
theia@theia-many37758:/home/project$ crontab -e
no crontab for theia - using an empty one
crontab: installing new crontab
theia@theia-many37758:/home/project$ echo -e "year\tmonth\tday\tobs_tmp\tfc_temp\taccuracy\taccuracy_range" > historical_fc_accuracy.tsv
theia@theia-many37758:/home/project$ echo '#!/bin/bash' > fc_accuracy.sh
theia@theia-many37758:/home/project$ echo '#!/bin/bash' > weekly_stats.sh
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMSkillsNetwork-LX0117EN-Coursera/labs/synthetic_historical_fc_accuracy.tsv
--2023-09-14 06:29:21--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMSkillsNetwork-LX0117EN-Coursera/labs/synthetic_historical_fc_accuracy.tsv
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 263 [text/tab-separated-values]
Saving to: ‘synthetic_historical_fc_accuracy.tsv’

synthetic_historical_fc 100%[===============================>]     263  --.-KB/s    in 0s      

2023-09-14 06:29:21 (31.3 MB/s) - ‘synthetic_historical_fc_accuracy.tsv’ saved [263/263]

theia@theia-many37758:/home/project$ chmod u+x weekly_stats.sh
theia@theia-many37758:/home/project$ ./rx_poc1.sh
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  9237  100  9237    0     0  21089      0 --:--:-- --:--:-- --:--:-- 21041
observed temperature = 22
theia@theia-many37758:/home/project$ chmod u+x fc_accuracy.sh
theia@theia-many37758:/home/project$ ./fc_accuracy.sh
Forecast accuracy is 2
theia@theia-many37758:/home/project$ ./weekly_stats.sh
-5
-1
-2
4
-2
0
1
-5
-1
-2
4
-2
0
1
minimum absolute error = 0
maximum absolute error = -5
theia@theia-many37758:/home/project$ 