# OLTP vs OLAP

## Side-by-Side Comparison

| Feature | OLTP | OLAP |
|---------|------|------|
| **Purpose** | Run transactions | Analyze data |
| **Operations** | INSERT, UPDATE, DELETE | SELECT with aggregations |
| **Query type** | Simple (one row) | Complex (millions of rows) |
| **Data size per query** | Small | Large |
| **Users** | Applications, end users | Analysts, managers |
| **Response time** | Milliseconds | Seconds to minutes |
| **Database type** | Row-based | Columnar |
| **AWS Services** | RDS, Aurora, DynamoDB | Redshift, Athena |

---

## Analogy

| OLTP | OLAP |
|------|------|
| Cash register (quick sale) | Annual sales report |
| ATM withdrawal | Bank's quarterly earnings |
| Adding item to cart | "Best-selling products this year" |

---

## Data Flow: OLTP → OLAP

In most systems, data flows from OLTP to OLAP:

```
User places order → OLTP (RDS) → ETL (Glue) → OLAP (Redshift) → Dashboard
```

1. The **OLTP system** handles the transaction
2. Data is **extracted and transformed**
3. Data goes into the **OLAP system** for analysis

---

## For the Exam

| Scenario | Use |
|----------|-----|
| "Handle millions of transactions per second" | OLTP (RDS, DynamoDB) |
| "Run complex analytics on historical data" | OLAP (Redshift, Athena) |
| "Low latency reads and writes" | OLTP |
| "Aggregate and report" | OLAP |

---

## Key Takeaway

> OLTP = fast transactions (RDS, DynamoDB). OLAP = complex analytics (Redshift, Athena). Data typically flows from OLTP to OLAP through ETL.

---

**Previous:** [OLAP Explained](./19-OLAP-Explained.md)
**Next:** [Section 03 — Data Formats](../03-Data-Formats/01-What-are-Data-Formats.md)
