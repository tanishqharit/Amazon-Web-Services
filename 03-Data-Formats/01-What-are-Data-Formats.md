# What are Data Formats?

## Simple Explanation

A **data format** is the way data is organized and stored in a file. Different formats are designed for different use cases.

Choosing the right format can make your data pipelines **faster, cheaper, and more efficient**.

---

## Why Data Formats Matter

| Bad format choice | Good format choice |
|-------------------|--------------------|
| Slow queries | Fast queries |
| High storage cost | Low storage cost |
| More data scanned | Less data scanned |
| Higher AWS bill 💸 | Lower AWS bill 💰 |

---

## Common Data Formats

| Format | Type | Best For |
|--------|------|----------|
| **CSV** | Text, row-based | Simple data exchange |
| **JSON** | Text, semi-structured | APIs, configuration |
| **Parquet** | Binary, columnar | Analytics, data lakes |
| **ORC** | Binary, columnar | Hive/EMR analytics |
| **Avro** | Binary, row-based | Streaming, schema evolution |

---

## Two Categories

### Row-based formats (CSV, Avro, JSON)
- Store data **row by row**
- Good for writing and reading **entire records**
- Used for transactional systems

### Columnar formats (Parquet, ORC)
- Store data **column by column**
- Good for **analytics** (you often query specific columns)
- Used for data lakes and warehouses

---

## Key Takeaway

> Data format choice directly impacts performance and cost. For analytics on AWS, columnar formats like Parquet are almost always the best choice.

---

**Next:** [CSV Format](./02-CSV-Format.md)
