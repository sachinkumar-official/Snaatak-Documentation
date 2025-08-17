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

## Introduction

This document serves as a proof of concept to demonstrate how to enable and use Git commit sign-offs effectively. It includes a step-by-step walkthrough for making sign-off commits, explains their significance, and provides references to further documentation and best practices.

---

## Understanding Commit Sign Off

*For understanding the concepts like what is commit sign-off, why we use sign-offs refer the document [here](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/SCRUM-150-sachin/Applications/CI-Design/Generic%20CI%20Operation/Commit%20Sign%20Off/Introduction/README.md)*

---

## Step by step walkthrough

### Step 1

*Go-to [github](www.github.com). Select the repository for which you want setup commit sign-off and clone it*

<img width="1087" height="133" alt="Image" src="https://github.com/user-attachments/assets/03566f0f-ce06-41c4-afe9-45d8f6033c64" />

### Step 2

*Make some changes*

<img width="812" height="267" alt="Image" src="https://github.com/user-attachments/assets/6c61967f-fe47-4c16-be96-547120adbecc" />

### Step 3

*Add the files to staging area. Now to commit with sign off use `-s` flag*
```
git commit -s -m "This commit-sign off demo"
```

<img width="1083" height="119" alt="Image" src="https://github.com/user-attachments/assets/52a3b5c6-606a-4c06-a396-81c1ed2ed720" />

### Step 4

*Push your changes to remote repository*

<img width="1083" height="182" alt="Image" src="https://github.com/user-attachments/assets/1fe6f72b-215a-40bf-8f5a-0819c607751a" />

### Step 5

*Confirm the changes*

<img width="1358" height="343" alt="Image" src="https://github.com/user-attachments/assets/7bc219c3-7bd8-402c-909f-2e3a6bee8bec" />

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
