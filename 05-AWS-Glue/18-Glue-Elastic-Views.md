# Glue Elastic Views

## What is Glue Elastic Views?

**Glue Elastic Views** was a preview feature that let you create **materialized views** across different data stores (DynamoDB → S3, for example).

---

## Current Status

⚠️ **Glue Elastic Views has been discontinued.** AWS removed it from the service.

---

## Why It's Mentioned

- Some older study materials still reference it
- The exam may not test it, but it's good to know it was replaced by other patterns

---

## What to Use Instead

| Need | Use |
|------|-----|
| Replicate DynamoDB to S3 | DynamoDB Streams + Lambda, or DynamoDB export to S3 |
| Materialized views | Redshift Materialized Views |
| Cross-service data sync | AWS Glue ETL jobs |

---

## Key Takeaway

> Glue Elastic Views was discontinued. If you see it in study materials, ignore it. Use Glue ETL, DynamoDB Streams, or Redshift Materialized Views instead.

---

**Previous:** [Glue Schema Registry](./17-Glue-Schema-Registry.md)
**Next:** [Glue Best Practices](./19-Glue-Best-Practices.md)
