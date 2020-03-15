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

-------------------
      NOTES        |
-------------------
 notes : 
 - the Maven Goal in this case is install Not package  because install means "deploy":either deploy yor artifact on the artifactory or maven local-artifactory
 - sonarqube in "Pre-Step" phase to test code quality (Quality Asurance) (QA) & it's configrations:
sonar.host.url=http://sonarqube:9000
sonar.projectKey=java-app1
sonar.sources=./src
sonar.language=java
- artifactory configured twice :
  1- at build Phase : to Resolve artifacts from Artifactory (store building-binaries in the artifactory to increase the latency at building)
  <br>2- at Post-Build Action : to deploy the artifact in the artifatory 
