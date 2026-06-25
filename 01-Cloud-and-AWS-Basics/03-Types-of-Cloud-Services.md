# Types of Cloud Services: IaaS, PaaS, SaaS

## The Three Layers

Think of cloud services like ordering food:

| Type | What You Get | Analogy |
|------|-------------|---------|
| **IaaS** | Raw infrastructure (servers, storage) | Buying groceries and cooking yourself |
| **PaaS** | Platform to build on (no server management) | Meal kit — ingredients given, you cook |
| **SaaS** | Ready-to-use software | Eating at a restaurant |

---

## IaaS — Infrastructure as a Service

**What it is:** You rent raw computing resources — virtual machines, storage, networking.

**You manage:** Operating system, apps, data
**Provider manages:** Hardware, networking, physical security

**AWS Examples:**
- Amazon EC2 (virtual servers)
- Amazon S3 (storage)
- Amazon VPC (networking)

**Use when:** You need full control over the infrastructure.

---

## PaaS — Platform as a Service

**What it is:** You get a platform to build and deploy apps. No need to manage servers.

**You manage:** Your code and data
**Provider manages:** Everything else (servers, OS, runtime)

**AWS Examples:**
- AWS Elastic Beanstalk
- AWS Lambda (serverless)
- Amazon RDS (managed database)

**Use when:** You want to focus on your code, not infrastructure.

---

## SaaS — Software as a Service

**What it is:** Ready-made software you use over the internet. No setup needed.

**You manage:** Just your data and settings
**Provider manages:** Everything

**Examples:**
- Gmail
- Netflix
- Slack
- Amazon QuickSight (AWS dashboarding tool)

**Use when:** You just want to use the software without building anything.

---

## Visual Comparison

```
What YOU manage vs What the PROVIDER manages:

IaaS:    [Apps | Data | Runtime | OS]  ←you    |  [Hardware | Network]  ←provider
PaaS:    [Apps | Data]  ←you                   |  [Runtime | OS | Hardware]  ←provider
SaaS:    [Data]  ←you                          |  [Everything else]  ←provider
```

---

## For the Exam

Most AWS data engineering services are **PaaS**:
- AWS Glue → PaaS (managed ETL)
- Amazon Redshift → PaaS (managed data warehouse)
- Amazon Athena → SaaS-like (just query, no servers)
- Amazon EC2 → IaaS (you manage the server)

---

## Key Takeaway

> IaaS = rent machines. PaaS = rent a platform. SaaS = rent software. Most AWS data services are PaaS — they handle the infrastructure so you focus on data.

---

**Previous:** [Benefits of Cloud Computing](./02-Benefits-of-Cloud-Computing.md)
**Next:** [What is AWS](./04-What-is-AWS.md)
