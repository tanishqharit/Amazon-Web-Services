# IAM Roles

## What is an IAM Role?

An **IAM Role** is a set of permissions that an **AWS service or application can assume temporarily**.

Think of it like a badge:
- A person (User) has a permanent ID card
- A Role is like a **temporary visitor badge** — you wear it when needed, then return it

---

## Why Roles Exist

IAM Users are for **people**. But what about AWS services?

For example:
- An **AWS Glue job** needs to read data from S3
- A **Lambda function** needs to write to DynamoDB
- An **EC2 instance** needs to access Redshift

These services can't type a password. Instead, they **assume a Role** to get temporary permissions.

---

## How Roles Work

```
1. You create a Role with specific permissions
2. You assign the Role to a service
3. The service "assumes" the Role
4. The service gets temporary credentials
5. These credentials expire automatically
```

---

## Users vs Roles

| Feature | IAM User | IAM Role |
|---------|----------|----------|
| For whom? | People, applications | AWS services, cross-account access |
| Credentials | Permanent (password, keys) | Temporary (auto-expire) |
| Example | "tanishq" logs in | Glue job reads S3 |

---

## Common Role Examples for Data Engineering

| Role | What it does |
|------|-------------|
| GlueServiceRole | Allows Glue to access S3 and the Data Catalog |
| LambdaExecutionRole | Allows Lambda to write to DynamoDB |
| RedshiftS3ReadRole | Allows Redshift to read from S3 |
| EMR_EC2_Role | Allows EMR instances to access S3 |

---

## For the Exam

- **Roles are the preferred way** to give AWS services permissions
- Never put access keys inside your code — use Roles instead
- Roles provide **temporary credentials** that auto-rotate

---

## Key Takeaway

> IAM Roles give AWS services temporary permissions. Always use Roles for service-to-service access. Never hardcode access keys.

---

**Previous:** [IAM Groups](./11-IAM-Groups.md)
**Next:** [IAM Policies](./13-IAM-Policies.md)
