


# Documentation on AMD-Based Instances

  <img width="400" height="215" alt="Image" src="https://github.com/user-attachments/assets/78ace518-17e4-4823-a7b1-3b35cf49a8f4" />

---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 29-08-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 29-08-2025      | V1.0    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|
---
## Table of Contents
- [Introduction](#introduction)
- [AMD-Based Instance Families](#amd-based-instance-families)
- [Cost-Performance Advantages](#cost-performance-advantages)
- [Software Compatibility](#software-compatibility)
- [Recommended Scenarios](#recommended-scenarios)
- [Conclusion](#conclusion)
- [Contact Information](#Contact-Information)
- [References](#references)
---

## Introduction
AWS offers AMD-based Amazon EC2 instances as a cost-effective alternative to traditional Intel-based instances. These instances leverage AMD EPYC processors, providing a balance of performance, scalability, and affordability. They are fully compatible with existing workloads and ideal for a wide range of use cases.

---

## AMD-Based Instance Families

| Instance Family | Key Features | Target Workload |
|-----------------|-------------|----------------|
| General Purpose (M6a, T4a) | Balanced CPU, memory, and network performance | Web servers, small-to-medium databases, development environments |
| Compute Optimized (C6a) | High CPU-to-memory ratio for compute-intensive tasks | Batch processing, HPC, scientific modeling, AI inference |
| Memory Optimized (R6a, X2a) | Large memory per vCPU for memory-intensive workloads | In-memory databases, big data analytics, caching |
| Storage Optimized (I4a) | High IOPS and storage throughput | Data warehousing, NoSQL databases, transactional systems |

---
## Cost-Performance Advantages

| Cost-Performance Advantages | Description |
|-----------------------------|-------------|
| Lower Pricing | AMD-based instances are often 10–20% cheaper than Intel equivalents. |
| High Performance per Dollar | Competitive clock speeds and core counts offer better price-to-performance ratio. |
| Energy Efficiency | AMD EPYC processors reduce operational costs. |
| Scalable Options | Wide range of sizes for small and large deployments. |

---
## Software Compatibility

| Software Category | Supported Software / Platforms |
|------------------|-------------------------------|
| Operating Systems | Linux distributions (Ubuntu, RHEL, CentOS, Amazon Linux), Windows Server |
| Databases | MySQL, PostgreSQL, MongoDB, Oracle, Microsoft SQL Server |
| Containers & Orchestration | Docker, Kubernetes |

---
## Recommended Scenarios

| Scenario | Description |
|---------|-------------|
| Cost-Sensitive Deployments | High performance at lower cost |
| Compute-Intensive Workloads | HPC simulations, batch processing, AI inference |
| Memory-Intensive Applications | In-memory databases, large analytics workloads |
| Development & Testing | Non-production environments requiring flexibility |
| Containerized Workloads | Microservices or Kubernetes clusters efficiently |

---

## Conclusion
AWS has server options that use AMD processors. These servers cost less money than the Intel versions. They are powered by AMD EPYC processors, which means they run quickly and powerfully, and can change size based on your needs. You can use them for all the same programs you run now, and they are good for many different jobs.

---
## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| **Sachin Kumar**  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |

---

## References

| Resource | Link |
|---------|------|
| **AWS EC2 AMD-Based Instances** | [Link](https://aws.amazon.com/ec2/instance-types/) |
| **AMD offical Document** | [Link](https://www.amd.com/en/ecosystem/csp/aws.html) |
