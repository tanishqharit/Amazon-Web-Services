# S3 Select

## What is S3 Select?

**S3 Select** lets you use **simple SQL** to retrieve only a **subset** of data from an object, instead of downloading the entire file.

---

## The Problem

Without S3 Select:
```
You need 3 columns from a 10 GB CSV file
→ Download all 10 GB
→ Filter in your application
→ Slow and expensive
```

With S3 Select:
```
You need 3 columns from a 10 GB CSV file
→ S3 filters server-side
→ Returns only the 3 columns (maybe 500 MB)
→ Fast and cheap
```

---

## Supported Formats

S3 Select works with:
- CSV
- JSON
- Parquet

---

## Example Query

```sql
SELECT name, age FROM s3object WHERE city = 'Delhi'
```

---

## Limitations

- Only **simple SQL** (no JOINs, no subqueries)
- Single file only (can't query across files)
- For complex queries → use **Amazon Athena** instead

---

## S3 Select vs Athena

| Feature | S3 Select | Athena |
|---------|-----------|--------|
| Query scope | Single object | Multiple objects/folders |
| SQL support | Basic | Full SQL |
| Use case | Filter one file fast | Analyze entire datasets |
| Setup | No setup | Define tables in Glue Catalog |

---

## Key Takeaway

> S3 Select filters data inside S3 before downloading, saving time and cost. Good for simple queries on single files. For complex analytics, use Athena.

---

**Previous:** [S3 Multipart Upload](./19-S3-Multipart-Upload.md)
**Next:** [S3 Object Lambda](./21-S3-Object-Lambda.md)
