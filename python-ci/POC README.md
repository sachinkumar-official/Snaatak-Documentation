
# POC of Dependency Scanning

<img width="366" height="236" alt="Image" src="https://github.com/user-attachments/assets/d0f55cc7-6fdb-4925-a4f7-160b59f7a209" />


---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 20-07-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 21-07-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|
---


## Table of Contents

- [Introduction](#introduction)  
- [What and Why Dependency Scanning?](#what-and-why-dependency-scanning)  
- [Pre-requisites](#pre-requisites)
- [Install Dependencies](#install-dependencies)
- [Running pip-audit](#running-pip-audit)
- [Analyzing Results](#analyzing-results)
- [Conclusion](#conclusion)  
- [Contact Information](#contact-information)  
- [References](#references)  

---

## Introduction

This document provides a step-by-step guide to perform dependency vulnerability scanning on Python projects using `pip-audit`. Finding known weaknesses in a project's dependencies allows developers to fix problems early and keep their applications safe and reliable.

---

## What and Why Dependency Scanning?

[Click here](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/SCRUM-168-sachin/Applications/CI-Design/Python%20CI%20Checks/Bugs%20analysis/Introduction/README.md) for a detailed and informative guide on dependency scanning with python.

---

## Steps of Conduct

### Pre-requisites

| Dependency       | Minimum Version |
|------------------|-----------------|
| Operating System | Ubuntu 22.04    |
| Python           | 3.8+            |
| pip              | 20.0+           |
| pip-audit        | Latest          |
| Git              | Latest          |

### Install Dependencies

1. **Check if pip3 is installed**

    ```
    pip3 --version
    ```
   <img width="527" height="75" alt="Image" src="https://github.com/user-attachments/assets/f58e682c-f120-4a63-aa07-47719236aacd" />


2. **Install pip (if not installed)**

    ```
    sudo apt update
    sudo apt install python3-pip
    ```
    >*If pip3 is not found, install it with:*

      <img width="801" height="201" alt="Image" src="https://github.com/user-attachments/assets/c1f70c2b-97f2-4955-b8c9-d65aaba7a6c9" />

    - **then check**
        
   ```
   pip3 --version
   ```

   <img width="801" height="68" alt="Image" src="https://github.com/user-attachments/assets/c8c4ba07-90f0-413c-a413-3e752d41eea9" />
  
3. **Install pip-audit**

   *Use pip to install a pip package*

   ```
   sudo pip install pip-audit --break-system-packages
   ```

   <img width="470" height="69" alt="Image" src="https://github.com/user-attachments/assets/cbbfe35c-8731-423f-a014-c2738d081624" />

### Running pip-audit

1. **Clone the Repositories**

    *Clone the [Notification API](https://github.com/OT-MICROSERVICES/notification-worker.git) and [Attendance API](https://github.com/OT-MICROSERVICES/attendance-api.git) from github.*

    <img width="759" height="281" alt="Image" src="https://github.com/user-attachments/assets/b5cdc931-9870-406f-9a44-f920a5a3393e" />



2. **Audit Dependencies**
  
  > **Attendance API**

  - *Create a virtual environment venv1 for Attendacne API and activate it*
    
    ```
    python3 -m venv venv1
    source venv1/bin/activate
    ```

    <img width="759" height="97" alt="Image" src="https://github.com/user-attachments/assets/f3c0eff8-2927-4074-b942-e8928a03fad3" />

  - *Check if requirement.txt exists. If not create a requirements.txt with:*
    ```
    pip freeze > requirements.txt
    ```
    
    <img width="769" height="33" alt="Image" src="https://github.com/user-attachments/assets/8eeffb49-2c00-4eba-96f1-6481e22596fb" />

    
    ```
    pip-audit -r requirements.txt
    ```
    
    <img width="773" height="73" alt="Image" src="https://github.com/user-attachments/assets/d66a8b6b-24fc-4363-96a8-2f14798ac9fe" />

  - *Deactivate the virtual environment*

    ```
    deactivate
    ```

    <img width="663" height="65" alt="Image" src="https://github.com/user-attachments/assets/0689ff4b-cefe-41a9-b89c-88a39ef6d5dc" />

  > **Notification Worker**

  - *Create a virtual environment venvn2 for notification worker and activate it*
    
    ```
    python3 -m venv venv2
    source venv2/bin/activate
    ```

    <img width="704" height="70" alt="Image" src="https://github.com/user-attachments/assets/e6ad5a52-f135-4685-9cce-6b734210de92" />

  - *Check if requirement.txt exists. If not create a requirements.txt with:*
       ```
       pip freeze requirements.txt
       ```
      <img width="1148" height="70" alt="Image" src="https://github.com/user-attachments/assets/2fd26aca-555c-454b-aa4f-26c46653cc98" />

    
    > *Already exists here*
    
  - *Audit the file.*
    
    ```
    pip-audit -r requirements.txt
    ```
    
    <img width="827" height="70" alt="Image" src="https://github.com/user-attachments/assets/acf2a726-9a51-4c61-9e7c-8f93dfbd529b" />

  - *Deactivate the virtual environment*

    ```
    deactivate
    ```

    <img width="1148" height="70" alt="Image" src="https://github.com/user-attachments/assets/2fd26aca-555c-454b-aa4f-26c46653cc98" />

### Analyzing Results

- **Review Vulnerabilities**

  Examine the output to identify packages with known vulnerabilities.

- **Update Insecure Packages**

  Modify `requirements.txt` to specify secure versions and update:

  ```bash
  pip install --upgrade -r requirements.txt
  ```

- **Re-run pip-audit**

  Ensure all vulnerabilities have been addressed:

  ```bash
  pip-audit -r requirements.txt
  ```
---

## Conclusion

Using pip-audit to scan projects like `attendance-api` and `notification-worker` finds known weaknesses in their dependencies. Fixing these flaws through regular checks and updates is a key step to keeping these applications secure.

---

## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |
---

## References

| Source                                                                                     | Description                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [pip-audit Documentation](https://pypi.org/project/pip-audit/)                             | Official guide for using pip-audit.                      |
| [GitHub - attendance-api](https://github.com/OT-MICROSERVICES/attendance-api.git)          | Repository for attendance-api project.                   |
| [GitHub - notification-worker](https://github.com/OT-MICROSERVICES/notification-worker.git)| Repository for notification-worker project.              |
