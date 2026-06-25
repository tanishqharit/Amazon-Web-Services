# AWS Availability Zones (AZs)

## What is an Availability Zone?

An **Availability Zone (AZ)** is one or more physical data centers within a Region.

Each Region has **at least 2-3 AZs**. They are separate buildings with their own power, cooling, and networking.

---

## How Regions and AZs Work Together

```
Region: us-east-1 (N. Virginia)
├── AZ: us-east-1a  (Data Center Group A)
├── AZ: us-east-1b  (Data Center Group B)
├── AZ: us-east-1c  (Data Center Group C)
├── AZ: us-east-1d  (Data Center Group D)
├── AZ: us-east-1e  (Data Center Group E)
└── AZ: us-east-1f  (Data Center Group F)
```

---

## Why AZs Matter

### Protection Against Failure

- If one AZ loses power → your app still runs in another AZ
- AZs are connected by **high-speed, low-latency** private network
- AZs are **physically separated** (different buildings, different power sources)

### Example

Imagine you run a database:
- **Single AZ** → If that data center catches fire, your database is gone
- **Multi-AZ** → Your database is copied to another AZ. If one fails, the other takes over automatically

---

## Key Concept: High Availability

**High Availability** = your system keeps working even if part of it fails.

How to achieve it:
- Deploy across **multiple AZs**
- AWS services like RDS, S3, and DynamoDB do this automatically

---

## For the Exam

- Amazon S3 stores data across **at least 3 AZs** automatically
- Amazon RDS supports **Multi-AZ** deployments for high availability
- Always think about **fault tolerance** when designing data pipelines

---

## Key Takeaway

> An AZ is a separate data center within a Region. Using multiple AZs protects your data and applications from failures. Most AWS managed services automatically use multiple AZs.

---

**Previous:** [AWS Regions](./05-AWS-Regions.md)
**Next:** [AWS Edge Locations](./07-AWS-Edge-Locations.md)
