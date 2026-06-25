# Principle of Least Privilege

## What is it?

The **Principle of Least Privilege** means:

> Give every user and service **only the permissions they need** to do their job — nothing more.

---

## Why It Matters

Imagine giving every employee the keys to every room in a building:
- The janitor can enter the CEO's office
- The intern can access the vault
- If any key is stolen, everything is at risk

Instead, give each person **only the keys they need**.

---

## Examples

### ❌ Bad Practice (Too Much Access)

```json
{
  "Effect": "Allow",
  "Action": "*",
  "Resource": "*"
}
```

This allows **everything on every resource**. Very dangerous.

### ✅ Good Practice (Least Privilege)

```json
{
  "Effect": "Allow",
  "Action": "s3:GetObject",
  "Resource": "arn:aws:s3:::sales-data-bucket/*"
}
```

This only allows **reading objects** from **one specific bucket**.

---

## How to Apply It

1. **Start with zero permissions** — deny everything by default
2. **Add permissions as needed** — only what the user/service requires
3. **Review regularly** — remove permissions that are no longer needed
4. **Use specific resources** — don't use `*` (wildcard) for resources

---

## For the Exam

This concept appears frequently:
- When asked how to **secure** a data pipeline → least privilege
- When a Glue job needs S3 access → give it a Role with **only** S3 read permissions
- When choosing between two solutions → pick the one with **fewer permissions**

---

## Key Takeaway

> Always give the minimum permissions needed. Start with nothing and add only what's required. This is a core security principle that the exam tests heavily.

---

**Previous:** [IAM Policies](./13-IAM-Policies.md)
**Next:** [AWS CLI Basics](./15-AWS-CLI-Basics.md)
