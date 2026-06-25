# Glue Databases and Tables

## Databases in Glue

A **Glue database** is just a **logical container** for grouping related tables. It doesn't store data — it organizes metadata.

```
Glue Data Catalog
├── Database: sales_db
│   ├── Table: orders
│   ├── Table: customers
│   └── Table: products
├── Database: marketing_db
│   ├── Table: campaigns
│   └── Table: ad_clicks
```

---

## Tables in Glue

A **Glue table** is a metadata definition that describes:

| Property | What it tells you |
|----------|-------------------|
| **Column names** | `order_id`, `customer_name`, `total` |
| **Data types** | `int`, `string`, `double` |
| **Data location** | `s3://bucket/raw/orders/` |
| **Data format** | Parquet, CSV, JSON |
| **Partitions** | `year`, `month` |
| **SerDe** | Serializer/Deserializer (how to read the format) |

**A Glue table does NOT contain data** — it just describes where data is and how to read it.

---

## Creating Tables

Two ways:

1. **Crawlers** — automatically discover and create tables
2. **Manual** — define the schema yourself in the console, CLI, or SDK

---

## Key Takeaway

> Glue databases group related tables. Glue tables are metadata definitions that point to your data in S3 or databases. They describe the schema, location, and format — not the actual data.

---

**Previous:** [Glue Crawlers](./03-Glue-Crawlers.md)
**Next:** [Glue ETL Jobs Overview](./05-Glue-ETL-Jobs-Overview.md)
