# IAM Policies

## What is an IAM Policy?

An **IAM Policy** is a JSON document that defines **what actions are allowed or denied** on which AWS resources.

Policies are the **actual rules**. Users, Groups, and Roles are useless without Policies attached to them.

---

## Policy Structure

A policy is written in JSON and has this structure:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-bucket/*"
    }
  ]
}
```

### Breaking it down:

| Field | Meaning |
|-------|---------|
| **Effect** | "Allow" or "Deny" |
| **Action** | What operation (e.g., `s3:GetObject` = read from S3) |
| **Resource** | Which resource (identified by its ARN) |

---

## Types of Policies

| Type | Description |
|------|------------|
| **AWS Managed Policies** | Pre-built by AWS (e.g., `AmazonS3ReadOnlyAccess`) |
| **Customer Managed Policies** | Created by you for custom needs |
| **Inline Policies** | Directly embedded in a User, Group, or Role |

**Best practice:** Use AWS Managed Policies when possible. Create custom ones only when needed.

---

## What is an ARN?

**ARN (Amazon Resource Name)** is a unique ID for any AWS resource.

Format: `arn:aws:service:region:account-id:resource`

Example: `arn:aws:s3:::my-data-bucket` identifies a specific S3 bucket.

---

## Policy Evaluation Rules

1. By default, everything is **denied**
2. An explicit **Allow** overrides the default deny
3. An explicit **Deny** always wins (overrides any Allow)

```
Default: DENY everything
+ Allow policy → Can access
+ Deny policy → Cannot access (even if Allow exists)
```

---

## Key Takeaway

> IAM Policies are JSON rules that define permissions. They have an Effect (Allow/Deny), Action (what), and Resource (which). Deny always wins over Allow.

---

**Previous:** [IAM Roles](./12-IAM-Roles.md)
**Next:** [Principle of Least Privilege](./14-Principle-of-Least-Privilege.md)
