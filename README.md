Jenkins/Java/Artifactory/Docker/Docker-compose/Selenium integration
This Project show how to connect between a java project in jenkins and Artifactory ( Repository Manager ) and SonarQube ( Code Quality ) also Docker/Docker-Compose and Selenium.

Configured Jobs

Simple Java app with Maven ( Building profile)
Java Artifactory integration
java Docker integration
Java SonarQube integration
Jenkins
port 8080
username: devops
password: devops
Artifactory
port: 9090
username: admin
password: password
SonarQube
-port: 9000

Docker
--> please check the docker-compose file "docker socket is mounted between host and container"

Selenium:
docker-compose file

if you are going yo use Ubuntu please do the following
rename docker-compose.yml-ubuntu docker-compose.yml --> note : it will use the Dockerfile