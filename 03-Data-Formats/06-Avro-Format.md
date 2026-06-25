# Avro Format

## What is Avro?

**Apache Avro** is a **row-based** binary format with a built-in schema. It's designed for **data serialization** and is great for **streaming** and **schema evolution**.

---

## How Avro is Different

| Feature | Parquet/ORC | Avro |
|---------|-------------|------|
| Storage | Columnar | Row-based |
| Best for | Analytics (read columns) | Streaming (write rows fast) |
| Schema | Embedded | Embedded + schema evolution |
| Speed | Fast reads | Fast writes |

---

## Schema Evolution

**Schema evolution** means changing the structure of your data without breaking existing data.

Example:
1. Version 1: `{ "name": "Tanishq", "age": 25 }`
2. Version 2: `{ "name": "Tanishq", "age": 25, "city": "Delhi" }`

Avro handles this smoothly — old data without "city" still works with the new schema.

---

## When to Use Avro

- **Streaming data** (Kinesis, Kafka) — fast row-by-row writes
- When your **schema changes frequently**
- For data that needs to be **written quickly** but read less often
- AWS Glue Schema Registry supports Avro

---

## For the Exam

| Scenario | Format |
|----------|--------|
| "Schema may change over time" | Avro |
| "Analytics on large datasets" | Parquet |
| "Streaming ingestion" | Avro |
| "Reduce query cost on Athena" | Parquet |

---

## Key Takeaway

> Avro is row-based and great for streaming and schema evolution. Use Avro for writing data fast and Parquet for reading data fast in analytics.

---

**Previous:** [ORC Format](./05-ORC-Format.md)
**Next:** [Row vs Columnar Formats](./07-Row-vs-Columnar-Formats.md)
