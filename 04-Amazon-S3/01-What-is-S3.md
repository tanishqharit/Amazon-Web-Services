# What is Amazon S3?

## Simple Explanation

**Amazon S3 (Simple Storage Service)** is an **object storage service** that lets you store and retrieve **any amount of data** from anywhere on the internet.

Think of S3 like an **infinite hard drive in the cloud**. You can store files of any type and any size.

---

## Why S3 is Important

S3 is the **foundation of data engineering on AWS**. Almost every data pipeline uses S3 at some point:

```
Data Sources → Store in S3 → Transform with Glue → Analyze with Athena
```

---

## Key Facts

| Feature | Detail |
|---------|--------|
| **Storage type** | Object storage (not file system, not block storage) |
| **Durability** | 99.999999999% (11 nines) — almost impossible to lose data |
| **Availability** | 99.99% uptime |
| **Max object size** | 5 TB per object |
| **Max upload (single PUT)** | 5 GB (use multipart upload for larger) |
| **Scaling** | Unlimited — store as much as you want |
| **Pricing** | Pay per GB stored + requests made |

---

## What S3 is NOT

- ❌ Not a file system (no folders in the traditional sense)
- ❌ Not a database (can't query rows directly — use Athena for that)
- ❌ Not block storage (that's EBS for EC2 instances)

---

## Common Uses in Data Engineering

| Use Case | How S3 is Used |
|----------|---------------|
| **Data Lake** | Central storage for all raw data |
| **ETL staging** | Land raw data before transforming |
| **Backup** | Archive old data cheaply |
| **Data sharing** | Share datasets between teams |
| **Query source** | Athena and Redshift Spectrum query S3 directly |

---

## Key Takeaway

> Amazon S3 is infinite, durable cloud storage. It's the backbone of every data lake on AWS. You'll use S3 in almost every data engineering pipeline.

---

**Next:** [S3 Buckets](./02-S3-Buckets.md)
