# What is AWS Glue?

## Simple Explanation

**AWS Glue** is a fully managed **serverless ETL (Extract, Transform, Load)** service. It helps you discover, prepare, move, and transform data for analytics.

Think of Glue as a **data factory** — raw materials (data) go in, processed goods (clean data) come out.

---

## Why Glue is Important

AWS Glue is the **most tested service** on the DEA-C01 exam. It covers:
- **Data Catalog** — central metadata store
- **Crawlers** — auto-discover data schemas
- **ETL Jobs** — transform data at scale
- **Data Quality** — validate your data

---

## Key Components

| Component | What it does |
|-----------|-------------|
| **Data Catalog** | Central metadata repository (schemas, tables, databases) |
| **Crawlers** | Scan data sources and populate the Catalog |
| **ETL Jobs** | Run code to transform data (Spark, Python, Ray) |
| **Triggers** | Start jobs on schedule or event |
| **Workflows** | Chain multiple jobs and crawlers together |
| **DataBrew** | Visual, no-code data preparation |
| **Schema Registry** | Manage and enforce schemas for streaming |

---

## Key Facts

| Feature | Detail |
|---------|--------|
| **Serverless** | No servers to manage |
| **Engine** | Apache Spark (for ETL jobs) |
| **Languages** | Python (PySpark) or Scala |
| **Pricing** | Pay per DPU-hour (Data Processing Unit) |
| **Data sources** | S3, RDS, DynamoDB, Redshift, JDBC databases |

---

## Key Takeaway

> AWS Glue is the Swiss Army knife of data engineering on AWS. It discovers schemas, transforms data, and manages metadata. Master Glue = master 34% of the exam (Domain 1).

---

**Next:** [Glue Data Catalog](./02-Glue-Data-Catalog.md)
