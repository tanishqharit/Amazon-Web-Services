# JSON Format

## What is JSON?

**JSON (JavaScript Object Notation)** is a text format that stores data as **key-value pairs**. It supports nesting and arrays.

---

## Example

```json
{
  "name": "Tanishq",
  "age": 25,
  "city": "Delhi",
  "skills": ["Python", "SQL", "AWS"]
}
```

---

## Characteristics

| Feature | JSON |
|---------|------|
| **Type** | Text, semi-structured |
| **Human-readable** | ✅ Yes |
| **Schema** | Flexible (no fixed schema) |
| **Supports nesting** | ✅ Yes |
| **Supports arrays** | ✅ Yes |
| **File size** | Large (lots of repeated keys) |

---

## Pros and Cons

**Pros:**
- ✅ Human-readable and easy to understand
- ✅ Supports complex, nested structures
- ✅ Used everywhere (APIs, web, databases)
- ✅ Flexible schema — each record can be different

**Cons:**
- ❌ Large file size (keys repeated in every record)
- ❌ Slow for analytics on large datasets
- ❌ Not columnar (must read entire records)

---

## JSON Lines (JSONL)

For big data, **JSON Lines** (one JSON object per line) is preferred:

```
{"name": "Tanishq", "age": 25}
{"name": "Priya", "age": 30}
{"name": "Rahul", "age": 28}
```

This makes it easier to process large files line-by-line.

---

## When to Use JSON

- API responses and requests
- Configuration files
- Streaming data (Kinesis records are JSON)
- **Convert to Parquet** before storing in data lakes

---

## Key Takeaway

> JSON is flexible and great for APIs and streaming, but it's too large and slow for analytics. Always convert JSON to Parquet for storage in S3.

---

**Previous:** [CSV Format](./02-CSV-Format.md)
**Next:** [Parquet Format](./04-Parquet-Format.md)
