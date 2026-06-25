# S3 Access Control Lists (ACLs)

## What are S3 ACLs?

**ACLs (Access Control Lists)** are an older way to control access to S3 buckets and objects. They are simpler but less powerful than bucket policies.

---

## ACLs vs Bucket Policies

| Feature | ACLs | Bucket Policies |
|---------|------|-----------------|
| Granularity | Basic (read/write/full) | Detailed (specific actions) |
| Format | Simple XML | JSON |
| Flexibility | Limited | Very flexible |
| AWS recommendation | ❌ Discouraged | ✅ Preferred |

---

## Important: ACLs Are Disabled by Default

Since April 2023, **new S3 buckets disable ACLs by default**. AWS recommends using **bucket policies and IAM policies** instead.

The setting is called **"Bucket owner enforced"** — this disables ACLs.

---

## When ACLs Might Still Appear

- Legacy systems that still use ACLs
- Granting access to **S3 log delivery** (server access logging)
- Very simple public access scenarios

---

## Key Takeaway

> ACLs are the old way to control S3 access. They are disabled by default now. Always use bucket policies and IAM policies instead. The exam may mention ACLs but prefers bucket policies.

---

**Previous:** [S3 Bucket Policies](./15-S3-Bucket-Policies.md)
**Next:** [S3 Event Notifications](./17-S3-Event-Notifications.md)
