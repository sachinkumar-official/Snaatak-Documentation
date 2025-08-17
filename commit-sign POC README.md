# POC of Commit Sign-Off

<img width="259" height="194" alt="Image" src="https://github.com/user-attachments/assets/7ca2962c-ad06-4422-b1b7-e8bf49a180ed" />

---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 24-07-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 25-07-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|

---

## Table of Contents

<details>
<summary>1. Overview</summary>

- [Introduction](#introduction)  
- [Understanding Commit Sign Off](#understanding-commit-sign-off)  

</details>

<details>
<summary>2. Step-by-Step Walkthrough</summary>

- [Step 1: Clone the Repository](#step-1)  
- [Step 2: Make Some Changes](#step-2)  
- [Step 3: Commit with Sign-Off](#step-3)  
- [Step 4: Push to Remote](#step-4)  
- [Step 5: Confirm the Changes](#step-5)  

</details>

<details>
<summary>3. Wrap-Up</summary>

- [Conclusion](#conclusion)  
- [Contact](#contact)  
- [References](#references)

</details>

---

## Introduction

This document serves as a proof of concept to demonstrate how to enable and use Git commit sign-offs effectively. It includes a step-by-step walkthrough for making sign-off commits, explains their significance, and provides references to further documentation and best practices.

---

## Understanding Commit Sign Off

*For understanding the concepts like what is commit sign-off, why we use sign-offs refer the document [here]()*

---

## Step by step walkthrough

### Step 1

*Go-to [github](www.github.com). Select the repository for which you want setup commit sign-off and clone it*

![image](https://github.com/user-attachments/assets/06d483ff-1a7d-4a9c-8266-fb75f73aa821)

### Step 2

*Make some changes*

![image](https://github.com/user-attachments/assets/04bc4b7d-375b-46ae-a1df-3d2c280ef5ef)

### Step 3

*Add the files to staging area. Now to commit with sign off use `-s` flag*
```
git commit -s -m "It's that simple to create a sign off commit"
```

![image](https://github.com/user-attachments/assets/ecc23020-c442-4d77-b252-8d3e3b90fbe7)

### Step 4

*Push your changes to remote repository*

![image](https://github.com/user-attachments/assets/f385f4b3-af63-4d88-a0af-d37ad46ec5f7)

### Step 5

*Confirm the changes*

![image](https://github.com/user-attachments/assets/65404d3a-4cdb-4656-b3c1-1c0569703fdc)

---

## Conclusion

Implementing Git commit sign-offs is simple yet impactful, making contributors explicitly acknowledge their compliance with the DCO. Through this proof of concept, we've walked through the end-to-end process—from repository selection to verifying sign-offs—helping developers integrate this essential practice into their daily workflows.

---
## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |

---

## References

| Resource                         | Link                                                |
|----------------------------------|-----------------------------------------------------|
| **Developer Certificate of Origin (DCO)** | [Visit](https://developercertificate.org/) |
| **Git Commit Sign-Off Documentation** | [Visit](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---signoff) |
| **Jenkins Pipeline Documentation** | [Visit](https://www.jenkins.io/doc/book/pipeline/) |
| **GitHub DCO Action**           | [Visit](https://github.com/probot/dco) |
