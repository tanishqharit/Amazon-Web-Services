# S3 One Zone-IA

## What is S3 One Zone-IA?

**S3 One Zone-IA** is like Standard-IA but stores data in **only one Availability Zone** instead of three.

This makes it **20% cheaper** than Standard-IA, but less durable — if that AZ is destroyed, your data is gone.

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Access** | Instant |
| **AZs** | 1 AZ only (not replicated) |
| **Storage cost** | ~20% cheaper than Standard-IA |
| **Retrieval fee** | Yes |
| **Durability** | 99.999999999% (within the single AZ) |
| **Availability** | 99.5% (lower than Standard-IA) |

---

## When to Use

- Data you can **re-create** if lost (e.g., processed results, thumbnails)
- Secondary copies of data
- Non-critical, infrequently accessed data
- Cost is the top priority and data loss is acceptable

---

## When NOT to Use

- ❌ Data that cannot be re-created
- ❌ Primary copies of important data
- ❌ Compliance-required data

---

## Key Takeaway

> One Zone-IA is the cheapest IA option but stores data in only one AZ. Use it only for re-creatable, non-critical data. If the AZ fails, data is lost.

---

**Previous:** [S3 Standard-IA](./07-S3-Standard-IA.md)
**Next:** [S3 Glacier Instant Retrieval](./09-S3-Glacier-Instant-Retrieval.md)
