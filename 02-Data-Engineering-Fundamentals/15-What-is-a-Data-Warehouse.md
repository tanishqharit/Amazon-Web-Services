# What is a Data Warehouse?

## Simple Explanation

A **data warehouse** is a system designed specifically for **analyzing large amounts of structured data**.

Unlike a data lake (which stores everything raw), a data warehouse stores **clean, structured, and organized data** optimized for queries.

---

## Key Characteristics

| Feature | Data Warehouse |
|---------|----------------|
| **Data format** | Structured only (rows and columns) |
| **Schema** | Schema-on-write (define structure before loading) |
| **Purpose** | Fast analytics and reporting |
| **Users** | Business analysts, BI tools |
| **Query language** | SQL |

---

## Data Warehouse on AWS

On AWS, the primary data warehouse is **Amazon Redshift**.

```
Data Sources → ETL (Glue) → Amazon Redshift → BI Tools (QuickSight)
```

---

## Benefits

- ✅ **Very fast queries** on large datasets
- ✅ **Optimized for analytics** (columnar storage)
- ✅ Supports complex SQL queries, joins, aggregations
- ✅ Structured and organized

---

## Limitations

- ❌ Only handles **structured data**
- ❌ Data must be **cleaned before loading** (schema-on-write)
- ❌ More **expensive** than a data lake
- ❌ Less **flexible** (can't store raw, messy data)

---

## Key Takeaway

> A data warehouse stores clean, structured data optimized for fast SQL queries. Amazon Redshift is the AWS data warehouse. It's great for analytics but only handles structured data.

---

**Previous:** [What is a Data Lake](./14-What-is-a-Data-Lake.md)
**Next:** [What is a Data Lakehouse](./16-What-is-a-Data-Lakehouse.md)
