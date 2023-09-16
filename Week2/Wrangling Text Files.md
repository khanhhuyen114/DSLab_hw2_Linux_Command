theia@theia-many37758:/home/project$ cd ~
theia@theia-many37758:~$ ls
docker-compose         lib           README.md
dsdriver               node_modules  skills-network-extension-v0.1.0.tgz
entrypoint.sh          package.json  src-gen
gen-webpack.config.js  plugins       webpack.config.js
javasharedresources    postgres      yarn.lock
theia@theia-many37758:~$ cat entrypoint.sh
#!/bin/bash

if [ -f "$IBMCLOUD_API_KEY_LOCATION" ]; then
  export IBMCLOUD_API_KEY=$(cat $IBMCLOUD_API_KEY_LOCATION)
fi

if [[ ! -z ${IBMCLOUD_API_KEY+x} && "${PRELAUNCH_K8S}" == "true"  ]]; then
  ibmcloud login -r us-south

  echo "Waiting for ${DOCKER_CERT_PATH}/ca.pem"
  timeout=5
  until [ -f ${DOCKER_CERT_PATH}/ca.pem ]
  do
    if [ "$timeout" == 0 ]; then
      echo "ERROR: Timeout while waiting for the file ${DOCKER_CERT_PATH}/ca.pem"
      break
    fi
    sleep 2
    echo "waiting..."
    ((timeout--))
  done

  if [ "$timeout" != 0 ]; then
    echo "${DOCKER_CERT_PATH}/ca.pem found"
    ibmcloud cr login
  fi

  # Set SN_ICR_NAMESPACE for the user
  export SN_ICR_NAMESPACE=$(ibmcloud cr namespace-list | grep sn-labs- | xargs)

  # This will upsert the "icr" secret
  kubectl create secret docker-registry icr --docker-server=us.icr.io --docker-username=iamapikey --docker-password=$IBMCLOUD_API_KEY -o yaml --save-config --dry-run=client | kubectl apply -f -

  # Set the SN context
  export SN_KUBECTL_CONTEXT=$(kubectl config current-context)

  if [ -z ${SN_ICR_NAMESPACE+x} ]; then
    echo "ERROR: SN_ICR_NAMESPACE not set"
    exit 1
  fi
fi

if [ ! -z ${DHT+x} ]; then
  DHT_DECODED=$(echo $DHT | base64 -d)
  DHT_PARTS=(${DHT_DECODED//:/ })

  docker login -u ${DHT_PARTS[0]} -p ${DHT_PARTS[1]}
  kubectl create secret docker-registry dh --docker-server=index.docker.io/v2 --docker-username=${DHT_PARTS[0]} --docker-password=${DHT_PARTS[1]}
fi

chmod go-r /etc/kube/config

export MONGO_PASSWORD="$(echo "$RANDOM-$USERNAME-$RANDOM" | base64 | cut -c1-16)"
export CASSANDRA_PASSWORD="$(echo "$RANDOM-$USERNAME-$RANDOM" | base64 | cut -c1-16)"
export MYSQL_PASSWORD="$(echo "$RANDOM-$USERNAME-$RANDOM" | base64 | cut -c1-16)"
export POSTGRES_PASSWORD="$(echo "$RANDOM-$USERNAME-$RANDOM" | base64 | cut -c1-16)"
export PGPASSWORD="$POSTGRES_PASSWORD"
export AIRFLOW_PASSWORD="$(echo "$RANDOM-$USERNAME-$RANDOM" | base64 | cut -c1-16)"
export _AIRFLOW_WWW_USER_PASSWORD="$AIRFLOW_PASSWORD"

export PATH=$PATH:/home/theia/.local/bin

sudo service cron start

yarn theia start /home/project --hostname=0.0.0.0 --port=$THEIA_LOCAL_PORT
theia@theia-many37758:~$ more entrypoint.sh
#!/bin/bash

if [ -f "$IBMCLOUD_API_KEY_LOCATION" ]; then
  export IBMCLOUD_API_KEY=$(cat $IBMCLOUD_API_KEY_LOCATION)
fi

if [[ ! -z ${IBMCLOUD_API_KEY+x} && "${PRELAUNCH_K8S}" == "true"  ]]; then
  ibmcloud login -r us-south

  echo "Waiting for ${DOCKER_CERT_PATH}/ca.pem"
  timeout=5
  until [ -f ${DOCKER_CERT_PATH}/ca.pem ]
  do
    if [ "$timeout" == 0 ]; then
      echo "ERROR: Timeout while waiting for the file ${DOCKER_CERT_PATH}/ca.pem"
      break
    fi
    sleep 2
    echo "waiting..."
    ((timeout--))
theia@theia-many37758:~$ less entrypoint.sh
theia@theia-many37758:~$ cd /home/project
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/usdoi.txt
--2023-09-15 23:07:19--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/usdoi.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8121 (7.9K) [text/plain]
Saving to: ‘usdoi.txt’

usdoi.txt               100%[===============================>]   7.93K  --.-KB/s    in 0s      

2023-09-15 23:07:19 (917 MB/s) - ‘usdoi.txt’ saved [8121/8121]

theia@theia-many37758:/home/project$ head usdoi.txt
The unanimous Declaration of the thirteen united States of America, When in the
Course of human events, it becomes necessary for one people to dissolve the
political bands which have connected them with another, and to assume among the
powers of the earth, the separate and equal station to which the Laws of Nature
and of Nature's God entitle them, a decent respect to the opinions of mankind
requires that they should declare the causes which impel them to the
separation.

We hold these truths to be self-evident, that all men are created equal, that
they are endowed by their Creator with certain unalienable Rights, that among
theia@theia-many37758:/home/project$ head -3 usdoi.txt
The unanimous Declaration of the thirteen united States of America, When in the
Course of human events, it becomes necessary for one people to dissolve the
political bands which have connected them with another, and to assume among the
theia@theia-many37758:/home/project$ tail usdoi.txt
People of these Colonies, solemnly publish and declare, That these United
Colonies are, and of Right ought to be Free and Independent States; that they
are Absolved from all Allegiance to the British Crown, and that all political
connection between them and the State of Great Britain, is and ought to be
totally dissolved; and that as Free and Independent States, they have full
Power to levy War, conclude Peace, contract Alliances, establish Commerce, and
to do all other Acts and Things which Independent States may of right do. And
for the support of this Declaration, with a firm reliance on the protection of
divine Providence, we mutually pledge to each other our Lives, our Fortunes and
our sacred Honor.
theia@theia-many37758:/home/project$ tail -2 usdoi.txt
divine Providence, we mutually pledge to each other our Lives, our Fortunes and
our sacred Honor.
theia@theia-many37758:/home/project$ wc usdoi.txt
 152 1330 8121 usdoi.txt
theia@theia-many37758:/home/project$ wc -l usdoi.txt
152 usdoi.txt
theia@theia-many37758:/home/project$ wc -w usdoi.txt
1330 usdoi.txt
theia@theia-many37758:/home/project$ wc -c usdoi.txt
8121 usdoi.txt
theia@theia-many37758:/home/project$ sort usdoi.txt

abolishing the forms to which they are accustomed. But when a long train of
absolute rule into these Colonies:
abuses and usurpations, pursuing invariably the same Object evinces a design to
and correspondence. They too have been deaf to the voice of justice and of
and magnanimity, and we have conjured them by the ties of our common kindred to
and of Nature's God entitle them, a decent respect to the opinions of mankind
and organizing its powers in such form, as to them shall seem most likely to
Appropriations of Lands.
are Absolved from all Allegiance to the British Crown, and that all political
Arms against their Country, to become the executioners of their friends and
as to render it at once an example and fit instrument for introducing the same
Brethren, or to fall themselves by their Hands.
causes; and accordingly all experience hath shewn, that mankind are more
....

theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/zoo.txt
--2023-09-15 23:12:14--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/zoo.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54 [text/plain]
Saving to: ‘zoo.txt’

zoo.txt                 100%[===============================>]      54  --.-KB/s    in 0s      

2023-09-15 23:12:14 (7.08 MB/s) - ‘zoo.txt’ saved [54/54]

theia@theia-many37758:/home/project$ cat zoo.txt
zebra
zebra
lion
lion
anaconda
zebra
zebra
lion
zebra
theia@theia-many37758:/home/project$ uniq zoo.txt
zebra
lion
anaconda
zebra
lion
zebra
theia@theia-many37758:/home/project$ uniq zoo.txt
zebra
lion
anaconda
zebra
lion
zebra
theia@theia-many37758:/home/project$ uniq zoo.txt
zebra
lion
anaconda
zebra
lion
zebra
theia@theia-many37758:/home/project$ grep people usdoi.txt
Course of human events, it becomes necessary for one people to dissolve the
people, unless those people would relinquish the right of Representation in the
firmness his invasions on the rights of the people.
to harrass our people, and eat out their substance.
the lives of our people.
Tyrant, is unfit to be the ruler of a free people.
theia@theia-many37758:/home/project$ grep -v login /etc/passwd
root:x:0:0:root:/root:/bin/bash
sync:x:4:65534:sync:/bin:/bin/sync
theia:x:1000:1000:,,,:/home/theia:/bin/bash
postgres:x:105:109:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
theia@theia-many37758:/home/project$ cut -c -2 zoo.txt
ze
ze
li
li
an
ze
ze
li
ze
theia@theia-many37758:/home/project$ cut -c 2- zoo.txt
ebra
ebra
ion
ion
naconda
ebra
ebra
ion
ebra
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/v4_new_content/labs/names_and_numbers.csv
--2023-09-15 23:26:19--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/v4_new_content/labs/names_and_numbers.csv
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 42 [text/csv]
Saving to: ‘names_and_numbers.csv’

names_and_numbers.csv   100%[===============================>]      42  --.-KB/s    in 0s      

2023-09-15 23:26:19 (7.14 MB/s) - ‘names_and_numbers.csv’ saved [42/42]

theia@theia-many37758:/home/project$ cat names_and_numbers.csv
John Fogerty, 555-1212
Jane Doe, 555-1312
theia@theia-many37758:/home/project$ cut -d "," -f2 names_and_numbers.csv
 555-1212
 555-1312
theia@theia-many37758:/home/project$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/zoo_ages.txt
--2023-09-15 23:31:55--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/zoo_ages.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 20 [text/plain]
Saving to: ‘zoo_ages.txt’

zoo_ages.txt            100%[===============================>]      20  --.-KB/s    in 0s      

2023-09-15 23:31:55 (4.04 MB/s) - ‘zoo_ages.txt’ saved [20/20]

theia@theia-many37758:/home/project$ paste zoo.txt zoo_ages.txt
zebra   17
zebra   12
lion    7
lion    4
anaconda        3
zebra   4
zebra   1
lion    0
zebra   1
theia@theia-many37758:/home/project$ paste -d "," zoo.txt zoo_ages.txt
zebra,17
zebra,12
lion,7
lion,4
anaconda,3
zebra,4
zebra,1
lion,0
zebra,1
theia@theia-many37758:/home/project$ cd ~
theia@theia-many37758:~$ pwd
/home/theia
theia@theia-many37758:~$ wc -l /etc/passwd file
  25 /etc/passwd
wc: file: No such file or directory
  25 total
theia@theia-many37758:~$ grep "not installed" /var/log/bootstrap.log
  Package libc6 is not installed.
  Package libdebconfclient0 is not installed.
  awk is not installed.
  Package awk is not installed.
  libbz2-1.0 is not installed.
  libc6 is not installed.
  liblzma5 is not installed.
  libselinux1 is not installed.
  libzstd1 is not installed.
  zlib1g is not installed.
  ...
theia@theia-many37758:~$ wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/top-sites.txt
--2023-09-15 23:35:12--  https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Bash%20Scripting/top-sites.txt
Resolving cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)... 169.63.118.104
Connecting to cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud (cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud)|169.63.118.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1311 (1.3K) [text/plain]
Saving to: ‘top-sites.txt’

top-sites.txt           100%[===============================>]   1.28K  --.-KB/s    in 0s      

2023-09-15 23:35:12 (195 MB/s) - ‘top-sites.txt’ saved [1311/1311]

theia@theia-many37758:~$ grep "org" top-sites.txt
en.wikipedia.org
wordpress.org
mozilla.org
pt.wikipedia.org
es.wikipedia.org
w3.org
wikimedia.org
creativecommons.org
fr.wikipedia.org
apache.org
id.wikipedia.org
de.wikipedia.org
theia@theia-many37758:~$ head -n 7 top-sites.txt
youtube.com
www.google.com
apple.com
microsoft.com
cloudflare.com
play.google.com
support.google.com
theia@theia-many37758:~$ tail -n 7 top-sites.txt
id.wikipedia.org
rakuten.co.jp
tinyurl.com
amazon.co.jp
de.wikipedia.org
tools.google.com
buydomains.comtheia@theia-many37758:~$ cut -c -3 top-sites.txt
you
www
app
mic
clo
pla
sup
www
en.
doc
...
theia@theia-many37758:~$ cd /home/project
theia@theia-many37758:/home/project$ cut -d "," -f1 names_and_numbers.csv
John Fogerty
Jane Doe
theia@theia-many37758:/home/project$ 