# Documentation of Commit Sign-Off 

---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 17-08-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 18-08-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|

---

## Introduction

This guide shows how to add a commit sign-off check to your app's CI setup.
It automatically verifies contributors and tracks changes better,
meeting your team's legal rules and quality standards.

---

## What is Commit Sign-Off?

Commit sign-off is a declaration by a contributor that they have the right to submit the code under the project’s license. It is included in the commit message using a line such as:

Signed-off-by: Developer Name <email@example.com>

It supports the Developer Certificate of Origin (DCO) and helps maintain accountability in both open-source and enterprise CI systems.

---

## Why Commit Sign-Off in CI?

Adding a sign-off check to your CI operations helps by:

- Enforcing project/license rules
- Prevents unauthorized code submissions
- Tracking who contributed what
- Making developers stand by their work
- Fitting smoothly into automated checks

---
## Workflow 


1. **Developer Commit**: The developer commits code with a mandatory `Signed-off-by` line.
2. **Pre-Check/Hook**: A Git hook or CI job verifies that each commit contains a valid sign-off.
3. **CI Pipeline Triggered**: If the sign-off passes, the CI pipeline is triggered automatically.
4. **Build and Test**: The application is built and tested in stages.
5. **Report and Notify**: The pipeline reports results and sends notifications. If sign-off is missing, the process halts early.

---
