# AWS Budgets and Cost Anomaly Alerts Implementation Guide

<img width="225" height="225" alt="Image" src="https://github.com/user-attachments/assets/153f2890-9a28-44cb-bb13-bdd4209b8cfb" />


---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 12-08-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 13-08-2025      | V1.0    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|
---

## Table of Contents

1. [Introduction](#introduction)
2. [Pre-requisites](#pre-requisites)
3. [Implementation](#implementation)
   - [Create a Budget Using a Template](#create-a-budget-using-a-template)
   - [Getting Started with AWS Cost Anomaly Detection](#getting-started-with-aws-cost-anomaly-detection)
4. [Best Practices](#best-practices)
5. [Contact Information](#contact-information)
6. [References](#references)

---

## Introduction

This guide details provide the step-by-step process to set up AWS Budgets and Cost Anomaly Alerts to monitor and control your cloud spending based on last sprint documentation.

> Here is link of Documentation. [Link](https://github.com/Snaatak-Apt-Get-Swag/documentation/blob/SCRUM-126-sachin/Cost-Optimization/Budget-And-Cost-Alerts/README.md)

---

## Pre-requisites

| Requirement                | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| AWS Account Access         | User must have access to the AWS account and Cost Management console.        |
| IAM Permissions            | Necessary permissions for managing Budgets and Cost Anomaly Detection.       |
| SNS/Email Setup            | Email addresses or SNS topics for notifications should be configured.        |
| Billing Enabled            | Ensure billing and cost management features are enabled on your AWS account. |

---


## Implementation

### Create a Budget Using a Template

1. Open the Billing and Cost Management console at [https://console.aws.amazon.com/cost-management/](https://console.aws.amazon.com/cost-management/).

   <img width="1364" height="662" alt="Image" src="https://github.com/user-attachments/assets/90e01fff-3a7b-4574-ac2f-a97dd91fed80" />


2. In the navigation pane, choose **Budgets**.

   <img width="392" height="577" alt="Image" src="https://github.com/user-attachments/assets/a398ebeb-5ebe-4907-a0f9-87b6eb6543bf" />

3. At the top of the page, choose **Create budget**.

   <img width="1017" height="577" alt="Image" src="https://github.com/user-attachments/assets/8f49a561-baac-4dc6-bf74-03c2aa34c717" />

4. Under **Budget setup**, choose **Use a template (simplified)**.

   <img width="1326" height="306" alt="Image" src="https://github.com/user-attachments/assets/44952eaf-e0ba-4f4e-828f-e764adcbf5a8" />

5. Under **Templates**, choose a template that best matches your use case:
    - **Zero spend budget**: A budget that notifies you after your spending exceeds AWS Free Tier limits.
    - **Monthly cost budget**: A monthly budget that notifies you if you exceed, or are forecasted to exceed, the budget amount.
    - **Daily Savings Plans coverage budget**: A coverage budget for your Savings Plans that notifies you when you fall below the defined target. This helps you to identify your on-demand spend sooner so that you can consider purchasing a new commitment.
    - **Daily reservation utilization budget**: A utilization budget for your Reserved Instances that notifies you when you fall below the defined target. This helps you to identify when you're not using some of your hourly commitment that you already purchased.

   <img width="1095" height="261" alt="Image" src="https://github.com/user-attachments/assets/dc627fdd-d888-49ea-beb4-b22ba78c93f2" />

6. Update the details and settings for your specific template.

   <img width="1095" height="444" alt="Image" src="https://github.com/user-attachments/assets/d61bbcbc-7792-4e8c-a170-3419e63fcd5d" />

7. Choose **Create budget**.

   <img width="1095" height="427" alt="Image" src="https://github.com/user-attachments/assets/53ac0aa4-10c6-4f18-8f40-484a4c4bdb4e" />

>Here is the Output.

   <img width="1363" height="292" alt="Image" src="https://github.com/user-attachments/assets/baa95a95-6f48-44db-bc6e-8a5b80637310" />


---

### Getting Started with AWS Cost Anomaly Detection

1. **Open Console**  
   Open the Billing and Cost Management console at [https://console.aws.amazon.com/cost-management/](https://console.aws.amazon.com/cost-management/).
2. **Navigate to Cost Anomaly Detection**  
   In the navigation pane, choose **Cost Anomaly Detection**.

   <img width="655" height="535" alt="Image" src="https://github.com/user-attachments/assets/01bcecb6-1d55-44e4-a9f6-36a63cbb3efa" />

3. **Open Cost Monitors Tab**  
   Choose the **Cost monitors** tab.

   <img width="888" height="508" alt="Image" src="https://github.com/user-attachments/assets/e5e23ffd-1047-4102-82e2-02ea1ef28e3d" />

4. **Create New Monitor**  
   Click **Create monitor**.

   <img width="883" height="384" alt="Image" src="https://github.com/user-attachments/assets/d964d89a-d1b5-483e-8fa1-858edff4cefc" />

5. **Choose Monitor Type & Name**  
   Select a monitor type.  
   Enter a short, descriptive Monitor name.

   <img width="1352" height="577" alt="Image" src="https://github.com/user-attachments/assets/60266046-8cee-4d85-872e-c6bb0a296ad7" />

6. **(Optional) Add Tags**  
   Add up to 50 key-value pair tags if needed.  
   Click **Next**.

   <img width="1352" height="278" alt="Image" src="https://github.com/user-attachments/assets/2904b8ce-48aa-49b6-8503-39b12a53015f" />

7. **Configure Alert Subscription**
   - Choose **Create a new subscription** or **Select an existing subscription**.
   - Enter a Subscription name.

   <img width="990" height="348" alt="Image" src="https://github.com/user-attachments/assets/86251678-126f-44db-adad-001318a1f44d" />

8. **Set Alert Frequency**  
   Choose **Individual alerts**, **Daily summaries**, or **Weekly summaries**.

   <img width="756" height="331" alt="Image" src="https://github.com/user-attachments/assets/b4a41ac8-c2d8-4a4a-8c0b-eecb0d4827a0" />

9. **Add Recipients**  
   Enter email addresses for receiving alerts.

   <img width="756" height="132" alt="Image" src="https://github.com/user-attachments/assets/51d03673-4b07-4d72-8270-6ab4c6e58f98" />

10. **Set Thresholds**
    - Choose **Absolute** or **Percentage** threshold.
    - (Optional) Add a second threshold and choose **AND/OR** condition.

   <img width="756" height="232" alt="Image" src="https://github.com/user-attachments/assets/c53dcd4e-cc0a-4620-a788-9f1d4e6b2cae" />

11. **Create Monitor**  
    Click **Create monitor** to finish.

   <img width="1087" height="242" alt="Image" src="https://github.com/user-attachments/assets/7c4c9966-7870-4e6f-849d-f77bb373447b" />

>Here is the Output.

   <img width="1363" height="582" alt="Image" src="https://github.com/user-attachments/assets/b712b040-8082-4707-adfc-3fa9cd2aec4c" />


---

## Best Practices

| Practice                     | Description                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------|
| Use Descriptive Names        | Name budgets and alerts clearly for easy identification.                                                       |
| Set Realistic Thresholds     | Define thresholds that reflect your organization's budget expectations.                                         |
| Regular Review               | Adjust thresholds and alert settings periodically based on actual usage.                                       |
| Integrate with Communication | Connect alerts to team communication tools (Slack, Email, etc.) for faster response.                           |
| Monitor Frequently           | Check and analyze anomalies regularly to avoid surprise charges.                                                |
| Document Changes             | Keep a log of all changes in budget and alert settings for audit and troubleshooting purposes.                  |

---

## Contact Information

| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |

---

## References

| Reference Name | Link | Description |
|:-------------- |:-----|:-----------|
| AWS Budgets Documentation | [AWS Budgets User Guide](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) | How to create, manage, and track AWS budgets. |
| AWS Cost Anomaly Detection | [AWS Cost Anomaly Detection](https://docs.aws.amazon.com/cost-management/latest/userguide/cost-anomaly-detection.html) | Machine learning-based cost anomaly detection in AWS. |
| AWS Cost Explorer | [AWS Cost Explorer](https://docs.aws.amazon.com/cost-management/latest/userguide/cost-explorer.html) | Visualize, understand, and manage your AWS costs and usage. |

---
