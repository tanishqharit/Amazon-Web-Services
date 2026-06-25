# What is IAM?

## Simple Explanation

**IAM (Identity and Access Management)** is the AWS service that controls **who can access what** in your AWS account.

Think of IAM like a security guard at a building:
- **Who are you?** (Authentication — proving your identity)
- **What are you allowed to do?** (Authorization — checking permissions)

---

## Why IAM is Important

Without IAM:
- Anyone could access your data
- Anyone could delete your servers
- Anyone could run up your AWS bill

With IAM:
- Each person gets their own login
- Each person only has permissions they need
- You can track who did what

---

## The Four Parts of IAM

| Part | What it is | Example |
|------|-----------|---------|
| **Users** | A person or application | "tanishq" — your personal login |
| **Groups** | A collection of users | "DataEngineers" group |
| **Roles** | Temporary permissions for services | Glue job needs to read S3 |
| **Policies** | Rules that define permissions | "Can read from S3 bucket X" |

---

## IAM is Global

- IAM is **not region-specific**
- Users, Groups, Roles, and Policies apply to **all Regions**
- This is different from most AWS services which are Region-specific

---

## IAM is Free

- IAM itself costs nothing
- You pay for the resources people access, not for IAM itself

---

## Key Takeaway

> IAM controls who can access your AWS resources and what they can do. It has Users, Groups, Roles, and Policies. IAM is global and free.

---

**Previous:** [AWS Management Console](./08-AWS-Management-Console.md)
**Next:** [IAM Users](./10-IAM-Users.md)
