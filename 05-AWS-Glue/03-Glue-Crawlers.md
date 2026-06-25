# Glue Crawlers

## What is a Crawler?

A **Glue Crawler** is a program that **automatically scans your data sources**, discovers the schema, and creates or updates table definitions in the **Glue Data Catalog**.

It saves you from manually defining schemas.

---

## How Crawlers Work

```
1. You point a Crawler at a data source (e.g., S3 path)
2. Crawler scans the data
3. Crawler figures out the schema (columns, data types)
4. Crawler creates/updates a table in the Data Catalog
5. Now Athena, Glue jobs, etc. can query the data
```

---

## What Crawlers Can Scan

| Data Source | Example |
|-------------|---------|
| **Amazon S3** | `s3://my-bucket/raw/sales/` |
| **Amazon RDS** | MySQL, PostgreSQL databases |
| **Amazon DynamoDB** | DynamoDB tables |
| **Amazon Redshift** | Redshift clusters |
| **JDBC databases** | Any database with a JDBC driver |

---

## Crawler Schedule

You can run crawlers:
- **On-demand** — manually when needed
- **On a schedule** — every hour, daily, weekly
- **On event** — triggered by S3 events (via EventBridge)

---

## What Happens with Schema Changes?

When a crawler runs again and finds changes:

| Change | Default behavior |
|--------|-----------------|
| New columns added | Adds them to the table |
| Columns removed | Keeps old columns (marks as missing) |
| New partitions | Adds new partitions |
| Data type changes | Can update or keep old type |

You can configure the **schema change policy** to control this behavior.

---

## Key Takeaway

> Crawlers scan data sources, discover schemas, and populate the Data Catalog automatically. Run them on schedule or on-demand. They save you from manually defining every table.

---

**Previous:** [Glue Data Catalog](./02-Glue-Data-Catalog.md)
**Next:** [Glue Databases and Tables](./04-Glue-Databases-and-Tables.md)
