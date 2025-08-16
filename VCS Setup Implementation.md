#  Implementation on VCS Setup 

<img width="314" height="160" alt="Image" src="https://github.com/user-attachments/assets/d14c27d8-1ed2-4b3c-9de8-d41c5cdb7aac" />

---
# Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 31-07-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 01-07-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|

---
# Table of Contents 
+ [Introduction](#Introduction)
+ [Prerequisites](#Prerequisites)
+ [Installation Setup](#Installation-Setup)
+ [Conclusion](#Conclusion)
+ [Contact Information](#Contact-Information)
+ [Reference](#Reference)
***


# Introduction

 This document will walk you through the step-by-step process of installing GitHub, an essential platform for version control and collaborative software development. GitHub is a web-based 
 platform and version control system that plays a crucial role in modern software development. It provides a collaborative environment for developers to host, manage, and share their code 
 repositories. 

***


# Prerequisites 

* Working Email ID 

***
# Setup via Web browser

## 1. Account Creation 

###  Sign Up for GitHub

- Go to [GitHub](https://github.com/).
- Click **Sign up**.
- Enter a valid email address, create a username, and set a strong password.
- Complete the verification (CAPTCHA and email confirmation).
- Once verified, log in to your GitHub account.

---

## 2. Organization Setup

Organizations are ideal if you plan to manage multiple repositories with collaborators.

### Create an Organization

- On GitHub, click your profile icon (top right) > **Your organizations**.
- Click **New organization**.
- Choose a plan (free for most users).
- Fill in organization name, email, and other details.
- Invite team members if needed.

---

## 3. Repository Creation

Repositories house your project files and code.

###  Create a Repository

- Inside your organization (or personal account), click **New repository**.
- Enter repository name, description, choose visibility (public/private).
- Initialize with a README (recommended).
- Add `.gitignore` and license if needed.

---

## 4. Team Management

Teams help organize contributors and manage permissions.

### Step 1: Create Teams

- Go to your organization > **Teams** > **New team**.
- Name your team (e.g., Developers, Designers, Testers).
- Add members to each team.

### Step 2: Assign Repository Access

- Assign teams to repositories.
- Set permissions (read, write, admin) based on role.
- Example: Developers get write access, Testers get read access.

---

## 5. Version Control Concepts

### Centralized VCS

- One central repository; all changes are committed to this server.
- Example tools: SVN, Perforce.

### Distributed VCS (Git/GitHub)

- Everyone has a local copy of the repository.
- Changes are made locally, then pushed to the remote repository.
- Collaboration is enhanced; no single point of failure.

### Local VCS

- Tracks changes only on your local machine.
- Not recommended for team projects.

#### Setting Up Git Locally

1. **Install Git**:  
   - Windows: [Install Guide](https://phoenixnap.com/kb/how-to-install-git-windows)  
   - Mac/Linux: Use your package manager (`brew install git` or `sudo apt install git`).

2. **Configure Git**:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

3. **Clone Repository**:
   ```bash
   git clone https://github.com/your-org/your-repo.git
   ```

4. **Branching and Merging**:
   ```bash
   git checkout -b feature-branch
   # Make changes
   git add .
   git commit -m "Description of changes"
   git push origin feature-branch
   # Create a Pull Request on GitHub
   ```

---

# Conclusion  

In conclusion, this GitHub Setup Documentation has guided you through the essential steps to establish a solid foundation for version control and collaborative development. GitHub's features will empower you to optimize your development workflow, collaborate efficiently, and maintain code quality. 

---
# Contact Information

| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |

---

# References

- [GitHub Docs](https://docs.github.com/en)
- [Git Installation Guide](https://phoenixnap.com/kb/how-to-install-git-windows)

---
