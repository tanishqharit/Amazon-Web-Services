# S3 Best Practices for Data Engineering

## Organizing Your Data Lake

```
s3://company-data-lake/
├── raw/           ← Land raw data here (original format)
├── processed/     ← Cleaned/transformed data (Parquet)
├── curated/       ← Business-ready data
└── archive/       ← Old data in Glacier
```

---

## Performance Best Practices

1. **Use Parquet format** — columnar, compressed, fast queries
2. **Partition your data** — by date, region, or category: `s3://bucket/year=2024/month=01/`
3. **Right-size files** — aim for 128 MB to 1 GB per file (avoid tiny files)
4. **Use multipart upload** for files > 100 MB
5. **Enable Transfer Acceleration** for distant uploads

---

## Cost Best Practices

1. **Use lifecycle policies** to move old data to cheaper tiers
2. **Use Intelligent-Tiering** when access patterns are unknown
3. **Delete incomplete multipart uploads** via lifecycle rules
4. **Use S3 Select** or Athena to avoid scanning full objects
5. **Compress data** (Snappy or Zstd)

---

## Security Best Practices

1. **Block public access** by default on all buckets
2. **Enable default encryption** (SSE-S3 or SSE-KMS)
3. **Enable versioning** for critical data
4. **Use bucket policies** to enforce HTTPS
5. **Enable CloudTrail** for S3 access logging
6. **Use VPC endpoints** to keep traffic private

---

## Exam Tips for S3

| Question Pattern | Answer |
|-----------------|--------|
| "Cheapest storage for archives" | Glacier Deep Archive |
| "Unknown access pattern" | Intelligent-Tiering |
| "Reduce Athena query cost" | Parquet + partitioning |
| "Protect against accidental delete" | Versioning + MFA Delete |
| "Trigger pipeline on file upload" | S3 Event Notifications |
| "Encrypt with audit trail" | SSE-KMS |
| "Cross-account access" | Bucket Policy |

---

## Key Takeaway

> S3 is the heart of your data lake. Use Parquet, partition your data, apply lifecycle policies, and secure everything with encryption and bucket policies. These practices directly impact exam answers.

---

**Previous:** [S3 Replication](./22-S3-Replication.md)
**Next:** [Section 05 — AWS Glue](../05-AWS-Glue/01-What-is-AWS-Glue.md)
