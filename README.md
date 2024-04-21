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
