# Glue Data Catalog

## What is the Glue Data Catalog?

The **Glue Data Catalog** is a **central metadata repository** — it stores information ABOUT your data (not the data itself).

Think of it like a **library catalog** — the catalog tells you which books exist, where they are, and what they're about. But it doesn't contain the actual books.

---

## What It Stores

| Metadata | Example |
|----------|---------|
| **Database names** | `sales_db`, `marketing_db` |
| **Table names** | `orders`, `customers` |
| **Column names and types** | `order_id (int)`, `customer_name (string)` |
| **Data location** | `s3://my-bucket/raw/sales/` |
| **Data format** | Parquet, CSV, JSON |
| **Partition info** | `year=2024/month=01/` |

---

## Who Uses the Data Catalog?

The catalog is shared across many AWS services:

```
                    ┌── Amazon Athena (SQL queries)
Glue Data Catalog ──┼── Amazon Redshift Spectrum
                    ├── Amazon EMR (Spark/Hive)
                    └── AWS Lake Formation
```

When you define a table in the Glue Catalog, **all these services can use it**.

---

## Key Concepts

- **Database** → A logical grouping of tables (just for organization)
- **Table** → Metadata definition (schema, location, format) — NOT actual data
- **Partition** → How data is split for performance (e.g., by date)

---

## Important: Catalog ≠ Data

The catalog stores **metadata only**. The actual data stays in S3, RDS, or wherever it lives. The catalog just points to it.

---

## Key Takeaway

> The Glue Data Catalog is a central metadata store that tells services WHERE data is, WHAT it looks like, and HOW to read it. Athena, Redshift Spectrum, and EMR all use it. It stores schemas, not data.

---

**Previous:** [What is AWS Glue](./01-What-is-AWS-Glue.md)
**Next:** [Glue Crawlers](./03-Glue-Crawlers.md)
