# OLAP Explained

## What is OLAP?

**OLAP (Online Analytical Processing)** is a system designed for **analyzing large amounts of data** to find patterns and insights.

Think of it like a business report:
- You're asking questions about **thousands or millions of records**
- "What were total sales last year?"
- "Which product sells best in Mumbai?"

---

## Characteristics

| Feature | OLAP |
|---------|------|
| **Purpose** | Analyze and report on data |
| **Operations** | SELECT with aggregations (SUM, AVG, COUNT) |
| **Speed** | Fast for complex queries on large data |
| **Data size** | Very large (millions to billions of rows) |
| **Users** | Analysts, managers, BI tools |
| **Example** | Sales trends, revenue reports |

---

## OLAP Example

```sql
-- Analyze total sales by region last quarter (OLAP query)
SELECT region, SUM(total) as total_sales
FROM orders
WHERE order_date BETWEEN '2024-10-01' AND '2024-12-31'
GROUP BY region
ORDER BY total_sales DESC;
```

This scans millions of rows and aggregates them — classic OLAP.

---

## AWS Services for OLAP

| Service | Type |
|---------|------|
| **Amazon Redshift** | Data warehouse for analytics |
| **Amazon Athena** | Serverless SQL on S3 |
| **Amazon EMR** | Big data analytics (Spark) |

---

## Key Takeaway

> OLAP is for analyzing large datasets with complex queries. Redshift and Athena are AWS OLAP services. OLAP answers business questions like "how much" and "what trends."

---

**Previous:** [OLTP Explained](./18-OLTP-Explained.md)
**Next:** [OLTP vs OLAP](./20-OLTP-vs-OLAP.md)
