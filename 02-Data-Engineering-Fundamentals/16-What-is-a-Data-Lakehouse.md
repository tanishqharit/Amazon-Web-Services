# What is a Data Lakehouse?

## Simple Explanation

A **data lakehouse** combines the best of both worlds:
- The **flexibility** of a data lake (store all data types cheaply)
- The **performance** of a data warehouse (fast queries with SQL)

---

## How It Works

```
Traditional:
Data Lake (S3) ──ETL──→ Data Warehouse (Redshift)  ← Two separate systems

Lakehouse:
Data Lakehouse (S3 + query engine) ← One unified system
```

In a lakehouse, data stays in the **data lake (S3)** but you can query it with **warehouse-like performance** using tools like Athena or Redshift Spectrum.

---

## Comparison

| Feature | Data Lake | Data Warehouse | Data Lakehouse |
|---------|-----------|----------------|----------------|
| Storage | All data types | Structured only | All data types |
| Cost | Low | High | Medium |
| Query speed | Slow (without optimization) | Very fast | Fast |
| Schema | On-read | On-write | Both |
| Best for | Storage, ML | BI, reports | Everything |

---

## Data Lakehouse on AWS

You can build a lakehouse on AWS using:

- **S3** for storage (the "lake" part)
- **Athena** or **Redshift Spectrum** for queries (the "warehouse" part)
- **AWS Glue** for ETL and the Data Catalog
- **Lake Formation** for governance

---

## Key Takeaway

> A data lakehouse combines the cheap storage of a data lake with the fast query power of a data warehouse. On AWS, you build it using S3 + Athena/Redshift Spectrum + Glue + Lake Formation.

---

**Previous:** [What is a Data Warehouse](./15-What-is-a-Data-Warehouse.md)
**Next:** [Data Lake vs Data Warehouse](./17-Data-Lake-vs-Data-Warehouse.md)
