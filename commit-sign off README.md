# Documentation of Commit Sign-Off 
<img width="259" height="194" alt="Image" src="https://github.com/user-attachments/assets/7ca2962c-ad06-4422-b1b7-e8bf49a180ed" />

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

  <img width="690" height="233" alt="Image" src="https://github.com/user-attachments/assets/14aa2e9e-4c90-43b4-8640-6f5e45b07642" />

1. **Developer Commit**: The developer commits code with a mandatory `Signed-off-by` line.
2. **Pre-Check/Hook**: A Git hook or CI job verifies that each commit contains a valid sign-off.
3. **CI Pipeline Triggered**: If the sign-off passes, the CI pipeline is triggered automatically.
4. **Build and Test**: The application is built and tested in stages.
5. **Report and Notify**: The pipeline reports results and sends notifications. If sign-off is missing, the process halts early.

---
## Advantages of Commit Sign-Off in CI

| Advantage                     | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| Traceability                  | Identifies the responsible developer for each commit.                      |
| Legal Clarity                 | Confirms contributor agreement to licensing terms.                         |
| Automation Friendly           | Easily validated by CI tools and Git hooks.                                |
| Policy Enforcement            | Enforces contribution rules at the source.                                 |
| Security & Compliance Support| Reduces risks of unauthorized contributions entering production.           |

---

## Proof of Concept

*Refer [this]() document to get a step-by-step guide to perform a Commit Sign-Off.*

---


## Best Practices

- Educate contributors on how and why to use sign-off
- Use automated CI checks or Git hooks to enforce sign-off
- Keep commit message format consistent
- Combine sign-off with mandatory code reviews
- Clearly document sign-off requirements in contribution guides

---

## Conclusion

Commit sign-off adds a critical compliance layer to the CI process. By verifying code ownership and policy agreement at the source, it strengthens the integrity and security of modern development workflows. When combined with automated CI checks, sign-off enforcement supports a scalable and reliable application CI design.

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
| **GitHub DCO Action**           | [Visit](https://github.com/probot/dco) |
