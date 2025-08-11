# AWS Budgets and Cost Anomaly Alerts Implementation Guide

| Created by     | Created on | Version | Last Updated On | Pre Reviewer   |
|----------------|------------|---------|-----------------|---------------|
| Nitin Sharma   | 11-08-2025 | V 1.0   | 11-08-2025      | Komal Jaiswal |

---

## Table of Contents

1. [Introduction](#introduction)
2. [Pre-requisites](#pre-requisites)
3. [Best Practices](#best-practices)
4. [Implementation](#implementation)
   - [Create a Budget Using a Template](#create-a-budget-using-a-template)
   - [Getting Started with AWS Cost Anomaly Detection](#getting-started-with-aws-cost-anomaly-detection)
5. [Contact Information](#contact-information)
6. [References](#references)

---

## Introduction

This guide details the step-by-step process to set up AWS Budgets and Cost Anomaly Alerts to monitor and control your cloud spending based on last sprint documentation.

---

## Pre-requisites

| Requirement                | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| AWS Account Access         | User must have access to the AWS account and Cost Management console.        |
| IAM Permissions            | Necessary permissions for managing Budgets and Cost Anomaly Detection.       |
| SNS/Email Setup            | Email addresses or SNS topics for notifications should be configured.        |
| Billing Enabled            | Ensure billing and cost management features are enabled on your AWS account. |

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

## Implementation

### Create a Budget Using a Template

1. Open the Billing and Cost Management console at [https://console.aws.amazon.com/cost-management/](https://console.aws.amazon.com/cost-management/).
2. In the navigation pane, choose **Budgets**.
3. At the top of the page, choose **Create budget**.
4. Under **Budget setup**, choose **Use a template (simplified)**.
5. Under **Templates**, choose a template that best matches your use case:
    - **Zero spend budget**: A budget that notifies you after your spending exceeds AWS Free Tier limits.
    - **Monthly cost budget**: A monthly budget that notifies you if you exceed, or are forecasted to exceed, the budget amount.
    - **Daily Savings Plans coverage budget**: A coverage budget for your Savings Plans that notifies you when you fall below the defined target. This helps you to identify your on-demand spend sooner so that you can consider purchasing a new commitment.
    - **Daily reservation utilization budget**: A utilization budget for your Reserved Instances that notifies you when you fall below the defined target. This helps you to identify when you're not using some of your hourly commitment that you already purchased.
6. Update the details and settings for your specific template.
7. Choose **Create budget**.

---

### Getting Started with AWS Cost Anomaly Detection

1. **Open Console**  
   Go to the AWS Billing and Cost Management console.
2. **Navigate to Cost Anomaly Detection**  
   In the navigation pane, choose **Cost Anomaly Detection**.
3. **Open Cost Monitors Tab**  
   Choose the **Cost monitors** tab.
4. **Create New Monitor**  
   Click **Create monitor**.
5. **Choose Monitor Type & Name**  
   Select a monitor type.  
   Enter a short, descriptive Monitor name.
6. **(Optional) Add Tags**  
   Add up to 50 key-value pair tags if needed.  
   Click **Next**.
7. **Configure Alert Subscription**
   - Choose **Create a new subscription** or **Select an existing subscription**.
   - Enter a Subscription name.
8. **Set Alert Frequency**  
   Choose **Individual alerts**, **Daily summaries**, or **Weekly summaries**.
9. **Add Recipients**  
   Enter email addresses for receiving alerts.
10. **Set Thresholds**
    - Choose **Absolute** or **Percentage** threshold.
    - (Optional) Add a second threshold and choose **AND/OR** condition.
11. **Create Monitor**  
    Click **Create monitor** to finish.

---

## Contact Information

| Name         | Email Address                                   |
|--------------|-------------------------------------------------|
| Nitin Sharma | [nitin.sharma.snaatak@mygurukulam.co](mailto:nitin.sharma.snaatak@mygurukulam.co) |

---

## References

- [AWS Budgets Documentation](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html)
- [AWS Cost Anomaly Detection](https://docs.aws.amazon.com/cost-management/latest/userguide/cost-anomaly-detection.html)
- For further details, see the attached PDF file and internal sprint documentation.
