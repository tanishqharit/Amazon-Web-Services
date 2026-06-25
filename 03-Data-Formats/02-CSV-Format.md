# CSV Format

## What is CSV?

**CSV (Comma-Separated Values)** is a simple text format where each line is a row and values are separated by commas.

---

## Example

```csv
name,age,city
Tanishq,25,Delhi
Priya,30,Mumbai
Rahul,28,Kolkata
```

---

## Characteristics

| Feature | CSV |
|---------|-----|
| **Type** | Text, row-based |
| **Human-readable** | ✅ Yes |
| **Schema** | No (just text) |
| **Compression** | Not built-in (can be gzipped) |
| **Supports nesting** | ❌ No |
| **File size** | Large |

---

## Pros and Cons

**Pros:**
- ✅ Very simple and widely supported
- ✅ Easy to create and read
- ✅ Works with Excel, databases, and most tools

**Cons:**
- ❌ No data types (everything is text)
- ❌ No schema enforcement
- ❌ Large file size compared to Parquet
- ❌ Slow for analytics on large datasets
- ❌ Commas in data can break the format

---

## When to Use CSV

- Quick data exchange between systems
- Small datasets
- Human-readable exports
- **Not recommended** for data lakes or analytics

---

## Key Takeaway

> CSV is simple and universal but inefficient for analytics. For data engineering on AWS, always convert CSV to Parquet or ORC for better performance.

---

**Previous:** [What are Data Formats](./01-What-are-Data-Formats.md)
**Next:** [JSON Format](./03-JSON-Format.md)
