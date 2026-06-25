# Data Lake vs Data Warehouse

## Quick Comparison

| Feature | Data Lake | Data Warehouse |
|---------|-----------|----------------|
| **Data type** | All (structured + unstructured) | Structured only |
| **Schema** | Schema-on-read | Schema-on-write |
| **Storage** | Cheap (S3) | Expensive (Redshift) |
| **Query speed** | Slower (unless optimized) | Very fast |
| **Users** | Data engineers, data scientists | Business analysts |
| **Processing** | ETL/ELT flexible | SQL-based |
| **AWS Service** | Amazon S3 | Amazon Redshift |

---

## When to Use a Data Lake

- You need to store **all types of data** (raw logs, images, JSON)
- You want **cheap, unlimited storage**
- You don't know yet how you'll use the data
- Data scientists need access to **raw data**

---

## When to Use a Data Warehouse

- You have **structured data** that's ready for analysis
- Business users need **fast SQL queries**
- You need to build **reports and dashboards**
- Data needs to be **clean and organized**

---

## Can You Use Both?

**Yes!** The most common pattern is:

```
Raw data → Data Lake (S3) → ETL (Glue) → Data Warehouse (Redshift) → Dashboards
```

- Data Lake = **storage** for everything
- Data Warehouse = **analytics** for structured, clean data

---

## Key Takeaway

> Data lakes store everything cheaply but query slowly. Data warehouses store structured data expensively but query fast. Most companies use both together.

---

**Previous:** [What is a Data Lakehouse](./16-What-is-a-Data-Lakehouse.md)
**Next:** [OLTP Explained](./18-OLTP-Explained.md)
