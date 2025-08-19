# POC of Bugs Analysis 

<img width="342" height="182" alt="Image" src="https://github.com/user-attachments/assets/d1fd4abf-6594-476b-9145-67c85337899e" /> <img width="242" height="208" alt="Image" src="https://github.com/user-attachments/assets/b419c48c-435d-4a69-99d0-e3fb1538df22" />

---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 19-08-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 20-08-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|
---

## Table Of Content

- [Introduction](#introduction)  
- [What and Why Bug Analysis?](#what-and-why-bug-analysis)  
- [Pre-requisites](#pre-requisites)
- [Install Dependencies](#install-dependencies)
- [Configuration](#configuration)
- [Service for SonarQube](#service-for-sonarqube)
- [Testing the API](#testing-the-api)
- [Conclusion](#conclusion)  
- [Contact Information](#contact-information)  
- [References](#references)  




## Introduction
This document offers a straightforward guide to identifying and addressing bugs in Java code. Implementing systematic bug analysis ensures that developers detect issues early, improve code reliability, and maintain application performance and security.

## What and Why Bug Analysis?

To get a detailed about bug analysis in java [click here](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/SCRUM-159-sachin/Applications/CI-Design/Java%20CI%20Checks/Bugs%20analysis/Introduction/README.md).

## Steps of Conduct

### Pre-requisites

| Dependency   | Minimum Version |
| ------------ | --------------- |
| Operating System | Ubuntu 22.04 |
| CPU    | 2 vCPU  |
| Hard Disk   | 25 GB  |
| RAM           | 4 GB     |
| Java JDK     | 17+             |
| PostgreSQL   | Latest Stable   |
| unzip        | Latest Stable   |
| SonarQube    | Latest Stable   |
| SonarScanner | Any Version   |
| Maven        | 3.6+            |
| SonarQube | 9000 (open)        |
| Secure HTTPS web traffic | 443  |       
| PostgreSQL database access | 5432  | 


### Install Dependencies

- **Update and Upgrade Packages**
  
   <img width="696" height="169" alt="Image" src="https://github.com/user-attachments/assets/6869852a-684b-49b2-b736-1ee7ae1b4b48" />

- **Install Java**

  *[Go to this link](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/89c6c6e8de0b6e6abbca8273c7f8ae0051f65c9b/Softwares/Java/Installation/Manual/README.md) and follow `Java Installation Steps (Ubuntu)`.*
  
  <img width="806" height="139" alt="Image" src="https://github.com/user-attachments/assets/67f409bc-a54a-4156-95a8-e7186ba7d96a" />


- **Install PostgreSQL**

  *[Go to this link](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/SCRUM-80-nitin/OT-Microservies/Softwares/Postgresql/POC/README.md) and follow `Step-by-Step Setup Guide`  step 6.*
  
  <img width="806" height="224" alt="Image" src="https://github.com/user-attachments/assets/9cf3626d-cfc8-4db2-93be-b9e1a4be3177" />


- **Install unzip**
    ``` 
    sudo apt install unzip -y
    unzip --version
    ```
   <img width="806" height="179" alt="Image" src="https://github.com/user-attachments/assets/87f89fbb-baee-453a-8f3c-b0f4f09cd93c" />

- **Install SonarQube**

  ```
  sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.3.79811.zip
  sudo unzip sonarqube-9.9.3.79811.zip
  sudo mv sonarqube-9.9.3.79811 /opt/sonarqube
  sudo groupadd sonar
  sudo useradd -d /opt/sonarqube -g sonar sonar
  sudo chown sonar:sonar /opt/sonarqube -R
  ```

   <img width="1307" height="366" alt="Image" src="https://github.com/user-attachments/assets/8469392a-3749-487a-8400-de3b2619575e" />

- **Install SonarScanner**

  ```
  cd /opt
  sudo wget "https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-7.1.0.4889-linux-x64.zip" -O sonar-scanner.zip
  sudo unzip sonar-scanner.zip
  sudo mv sonar-scanner-7.1.0.4889-linux-x64 sonar-scanner
  sudo chown -R $USER:$USER sonar
  echo "export PATH=$PATH:/opt/sonar-scanner/bin" >> ~/.bashrc
  source ~/.bashrc
  ```

  <img width="968" height="164" alt="Image" src="https://github.com/user-attachments/assets/307800be-4b6f-4d0d-b7e2-aee2340861e5" />
- **Install Maven**

  *Install Maven* [Go to this link](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/scrum-34-mansoor/Softwares/Java/Maven/SOP/README.md) and follow `Step 2: Install Maven and check version`.

  <img width="837" height="164" alt="Image" src="https://github.com/user-attachments/assets/1c594fd8-02f1-4d55-a0dd-f1f6d008c751" />

### Configuration

- **PostgreSQL**-

  > *Change postgre default password*

  ```
  sudo passwd postgres
  ```

  <img width="469" height="118" alt="Image" src="https://github.com/user-attachments/assets/a5f62b93-b369-4d5f-9611-4ea303b89e81" />
  

   > *Access postgre user*

  ```
  su - postgres
  ```

  <img width="469" height="73" alt="Image" src="https://github.com/user-attachments/assets/189a4958-a026-4fb5-9fc3-82073fcf5667" />

  > *Create a user sonar*

  ```
  createuser sonar
  ```

  <img width="469" height="73" alt="Image" src="https://github.com/user-attachments/assets/c01a096d-d9eb-4669-bc02-6623a953b420" />

  > *Log in to PostgreSQL and create database*

  ```
  psql
  
  ALTER USER sonar WITH ENCRYPTED PASSWORD 'sonar';
  CREATE DATABASE sonarqube OWNER sonar;
  GRANT ALL PRIVILEGES ON DATABASE sonarqube to sonar;
  ```
  
  <img width="636" height="181" alt="Image" src="https://github.com/user-attachments/assets/6961ca15-ac89-43fe-9859-c620ea8174c9" /> 
  
  ```
  \q
  exit
  ```

  <img width="389" height="111" alt="Image" src="https://github.com/user-attachments/assets/fa668a45-7a37-4236-8b76-9a0a2510a470" />

- **SonarQube**

  > *Edit the configuration file at `/opt/sonarqube/conf/sonar.properties` and add these database settings`*
  
  ```
  sonar.jdbc.username=sonar
  sonar.jdbc.password=sonar
  sonar.jdbc.url=jdbc:postgresql://localhost:5432/sonarqube
  ```

  <img width="988" height="385" alt="Image" src="https://github.com/user-attachments/assets/c9f82c43-866e-4203-acac-79f1e6025734" />
  
  > *Modify Kernel System Limits at `/etc/sysctl.conf`*
    ```
    vm.max_map_count=262144
    fs.file-max=65536
    ulimit -n 131072
    ulimit -u 8192
    ```

    <img width="683" height="286" alt="Image" src="https://github.com/user-attachments/assets/0485e103-8077-47fc-9794-aec2c5078be4" />


  > *Reboot the system to apply the changes*
  ```
  sudo reboot
  ```

- **SonarScanner**

  > *Edit the configuration file at `/opt/sonar-scanner/conf/sonar-scanner.properties` and add your SonarQube server URL*

  ```
  sonar.host.url=http://localhost:9000
  ```

  <img width="528" height="172" alt="Image" src="https://github.com/user-attachments/assets/d8d7d7c3-5ab9-44db-835b-bb85a9117efd" />


### Service for SonarQube

*Create a file at `/etc/systemd/system/sonarqube.service` and add the below block*

```
[Unit]
Description=SonarQube service
After=syslog.target network.target

[Service]
Type=forking
User=sonar
Group=sonar
ExecStart=/opt/sonarqube/bin/linux-x86-64/sonar.sh start
ExecStop=/opt/sonarqube/bin/linux-x86-64/sonar.sh stop
StandardOutput=journal
LimitNOFILE=131072
LimitNPROC=8192
TimeoutStartSec=5
Restart=always
SuccessExitStatus=143

[Install]
WantedBy=multi-user.target
```
  <img width="886" height="450" alt="Image" src="https://github.com/user-attachments/assets/5c19d5b0-f736-409a-9438-8d0ee991e09a" />


*Start the server*

```
sudo systemctl daemon-reload
sudo systemctl start sonarqube
sudo systemctl enable sonarqube
```

 <img width="886" height="232" alt="Image" src="https://github.com/user-attachments/assets/b9f4559b-c116-4250-b500-cc6e89468b43" />

### Testing the API  

*Clone your [Salary API](https://github.com/OT-MICROSERVICES/salary-api.git) project repository from GitHub*

  <img width="886" height="210" alt="Image" src="https://github.com/user-attachments/assets/2858e269-a424-40f2-99e6-a6e53a938df0" />

- **Start SonarQube Server**  

 > *Go-to SonarQube server at `<public-ip>:9000`*

    <img width="1361" height="415" alt="Image" src="https://github.com/user-attachments/assets/2b552ef6-2544-436d-92e7-0d89c009bcf6" />

- **Generate SonarQube Authentication Token**  

 > *Create an authentication token for scanning. `My Account > Security`*

 <img width="1361" height="573" alt="Image" src="https://github.com/user-attachments/assets/e6770544-cee6-451c-9194-8dbc9950bbdd" />

- **Configure the Project for SonarQube**

 > *Add SonarQube plugin configuration to Salary-API pom.xml.*
 
 ```
 <plugin>
      <groupId>org.sonarsource.scanner.maven</groupId>
      <artifactId>sonar-maven-plugin</artifactId>
      <version>3.9.1.2184</version>
 </plugin>
 ```

   <img width="1361" height="219" alt="Image" src="https://github.com/user-attachments/assets/e5df58cc-534b-4b2c-a077-c1a242bab4bf" />


- **Run Sonar Scanner**  

 > *Execute SonarScanner to analyze the code and send results to SonarQube.*
 ```
 mvn clean verify -DskipTests sonar:sonar \
  -Dsonar.projectKey=salary-api \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=sqa_d454c3fc62931070e4d56d27884ef13519fe5d0e # Your token generated in SonarQube
 ```

- **Analyze SonarQube Dashboard**  

 > *Review bugs, vulnerabilities, and other code quality metrics in the dashboard.*

 <img width="1361" height="706" alt="Image" src="https://github.com/user-attachments/assets/a7dfa5a9-0c14-42fa-b4c3-7de33fa51fdc" />

- **Prioritize and Fix Issues**  

 > *Address critical bugs and refactor code as needed.*

- **Document and Share Findings**  

 > *Summarize the bug analysis results for the team.*


## Conclusion  
Among the various tools discussed, **SonarQube** stands out due to its ability to perform both static and dynamic analysis, offer detailed dashboards, and integrate well with CI/CD pipelines. It is highly recommended for medium to large Java projects for continuous bug tracking and quality monitoring.

---
## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |
---

## References  

| Source                                                                                     | Description                                              |
| ------------------------------------------------------------------------------------------ | -------------------------------------------------------- |
| [SonarQube Official Documentation](https://docs.sonarqube.org/latest/)                     | Official guide for configuring and using SonarQube.      |
| [Java SE Development Kit (JDK) Downloads](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) | Download page for Java Development Kit (JDK 11).         |
| [Apache Maven Project](https://maven.apache.org/)                                          | Official website for Maven build automation tool.        |
| [Gradle Build Tool](https://gradle.org/)                                                   | Official site for the Gradle build automation system.    |
| [GitHub - Cloning a Repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) | Documentation on how to clone repositories from GitHub.  |
| [AWS EC2 Security Groups - Managing Inbound Rules](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html#security-group-rules) | AWS guide for configuring inbound rules in security groups. |
 
