# Integration-with-Jenkins

MAVEN 

Maven plugin install in Jenkins --> Manage Jenkins--->Manage Plugin-->click --> Go to Available Tab--->search Maven
Maven Integration click--->install without restart
Manage Jenkins---->{[Global Tool configuartion]}--->Ctrl + F--->search Maven
Jenkins file--->maven3 that is alais name this is you want to give and maven location mention finally saved
---------

DOCKER 

First Github sigup--->login completed
Below I pass the github password varible --->>Manage Jenkins--->{(Manage credential)}--->Jenkins--->{(Global credential)}--->add credential
Below click secret text---->id- dockerpass,pass - my pass of dockerhub
Click ok
Now paste groovy script in pipeline--->buildnow
It get error because file permission check from console output
chmod 777 /var/run/docker.sock
-----------

SONARQUBE

install mysql in Ubuntu
Step 1 — sudo apt-get install openjdk-11-jdk -y
Step 2 - Installing MySQL --> Then install the mysql-server package --> sudo apt install mysql-server
step 3 - Ensure that the server is running using the systemctl start command --> sudo systemctl start mysql.service
step 4 - wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.6.1.59531.zip
step 5 - sudo apt-get install zip -y
step 6 - In root user - without /opt path - mysql -h (DATABASE ENDPOINT) -P 3306 -u admin -p
mysql -h mysonar.cur9sziy6ysl.ap-south-1.rds.amazonaws.com -P 3306 -u admin -p
step 7-  edit wrapper.conf & sonar.properties
step 9 - sudo update-alternatives --config java
   /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.372.b07-1.amzn2.0.1.x86_64/jre/bin/java
step 9-  edit wrapper.conf 
step -10 root la --> chown -R ubuntu:ubuntu /opt/sonarqube-6.7.6
exit
It switch as a --> ec2/ubuntu user mode
step 11- Should be in ec2/ubuntu user mode --> go to /opt/bin/linux83 path---> then restart--> ./soanr.sh start
#Put command and execute  in mysql - mysql command
CREATE DATABASE sonar CHARACTER SET utf8 COLLATE utf8_general_ci;
CREATE USER sonar@localhost IDENTIFIED BY 'sonar';
CREATE USER sonar@'%' IDENTIFIED BY 'sonar';
GRANT ALL ON sonar.* TO sonar@localhost;
GRANT ALL ON sonar.* TO sonar@'%';
--------------

------------
