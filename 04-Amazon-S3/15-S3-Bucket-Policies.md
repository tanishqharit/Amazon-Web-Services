# S3 Bucket Policies

## What is a Bucket Policy?

A **bucket policy** is a JSON document attached to an S3 bucket that defines **who can do what** with the bucket and its objects.

It works like an IAM policy but is **attached to the bucket**, not the user.

---

## Example Policy

Allow anyone to read objects from a public bucket:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-public-bucket/*"
    }
  ]
}
```

---

## Key Fields

| Field | Meaning |
|-------|---------|
| **Effect** | Allow or Deny |
| **Principal** | Who (user, account, or `*` for everyone) |
| **Action** | What action (e.g., `s3:GetObject`, `s3:PutObject`) |
| **Resource** | Which bucket/objects |
| **Condition** | Optional conditions (IP address, HTTPS only, etc.) |

---

## Common Use Cases

| Use Case | Policy Action |
|----------|--------------|
| Make bucket public | Principal: `*`, Action: `s3:GetObject` |
| Force HTTPS only | Condition: `aws:SecureTransport = false` → Deny |
| Cross-account access | Principal: another AWS account ID |
| Restrict to specific IPs | Condition: `aws:SourceIp` |
| Force encryption | Deny PutObject without encryption headers |

---

## Bucket Policy vs IAM Policy

| Feature | Bucket Policy | IAM Policy |
|---------|--------------|------------|
| Attached to | S3 bucket | IAM user/role/group |
| Controls | Access to that bucket | Access across all services |
| Cross-account | ✅ Yes | Needs role assumption |

---

## Key Takeaway

> Bucket policies control access at the bucket level. They use JSON with Principal, Action, Effect, and Resource. Use them for cross-account access, public access, and enforcing encryption/HTTPS.

---

**Previous:** [S3 Encryption](./14-S3-Encryption.md)
**Next:** [S3 Access Control Lists](./16-S3-Access-Control-Lists.md)
