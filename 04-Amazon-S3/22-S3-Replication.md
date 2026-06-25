# S3 Replication

## What is S3 Replication?

**S3 Replication** automatically copies objects from one bucket to another. You can replicate within the same Region or across Regions.

---

## Two Types

| Type | Name | Use Case |
|------|------|----------|
| **CRR** | Cross-Region Replication | Copy to a different Region |
| **SRR** | Same-Region Replication | Copy within the same Region |

---

## Requirements

- **Versioning must be enabled** on both source and destination buckets
- Proper **IAM permissions** for S3 to replicate
- Can replicate to a bucket in a **different AWS account**

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Existing objects** | NOT replicated automatically (only new objects) |
| **Delete markers** | Can optionally be replicated |
| **No chaining** | Bucket A → B → C does NOT work (A only goes to B) |
| **Latency** | Near real-time (most objects within 15 minutes) |

---

## When to Use CRR (Cross-Region)

- **Compliance** — keep a copy in another Region
- **Lower latency** — serve data closer to users in another Region
- **Disaster recovery** — protect against Regional failures

## When to Use SRR (Same-Region)

- **Log aggregation** — collect logs from multiple buckets into one
- **Data processing** — replicate between dev and prod environments
- **Compliance** — keep a copy in a separate account

---

## Key Takeaway

> Replication copies objects between buckets automatically. CRR = cross-Region, SRR = same-Region. Versioning is required. Existing objects are NOT replicated — only new ones.

---

**Previous:** [S3 Object Lambda](./21-S3-Object-Lambda.md)
**Next:** [S3 Best Practices](./23-S3-Best-Practices.md)
