# AWS SDKs

## What is an AWS SDK?

An **SDK (Software Development Kit)** is a library/package that lets you **interact with AWS services using code**.

Instead of clicking in the Console or typing CLI commands, you write code:

```python
import boto3

s3 = boto3.client('s3')
response = s3.list_buckets()
print(response['Buckets'])
```

---

## Available SDKs

AWS has SDKs for many programming languages:

| Language | SDK Name |
|----------|----------|
| **Python** | **Boto3** (most popular for data engineering) |
| Java | AWS SDK for Java |
| JavaScript | AWS SDK for JavaScript |
| Go | AWS SDK for Go |
| .NET | AWS SDK for .NET |

---

## Why Boto3 Matters for Data Engineers

- Glue ETL jobs are written in **Python** (using Boto3)
- Lambda functions often use **Python + Boto3**
- Data pipeline automation scripts use **Boto3**

---

## Console vs CLI vs SDK

| Method | Best for |
|--------|---------|
| Console | Learning, one-time tasks |
| CLI | Quick commands, shell scripts |
| SDK (Boto3) | Building applications, automation, ETL code |

---

## Key Takeaway

> AWS SDKs let you use AWS services from your code. Boto3 (Python) is the most important SDK for data engineering. Glue and Lambda both use Python/Boto3.

---

**Previous:** [AWS CLI Basics](./15-AWS-CLI-Basics.md)
**Next:** [AWS Free Tier](./17-AWS-Free-Tier.md)
