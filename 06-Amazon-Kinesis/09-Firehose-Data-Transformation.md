# Firehose Data Transformation

## How Firehose Transforms Data

Firehose can invoke an **AWS Lambda function** to transform each record before delivery.

---

## How It Works

```
Raw data → Firehose → Lambda function → Transformed data → Destination (S3)
```

---

## What Lambda Can Do

- Add/remove/modify fields
- Filter out unwanted records
- Enrich data (add timestamps, lookup values)
- Convert formats
- Mask sensitive data (PII)

---

## Lambda Response Format

Lambda must return each record with a **status**:

| Status | Meaning |
|--------|---------|
| `Ok` | Record processed successfully |
| `Dropped` | Record intentionally skipped |
| `ProcessingFailed` | Record failed (goes to error output) |

---

## Format Conversion (No Lambda Needed)

Firehose can also convert data format **without Lambda**:

- **JSON → Parquet** ⭐ (most common)
- **JSON → ORC**

This uses the **Glue Data Catalog** table schema for conversion.

---

## For the Exam

- "Convert JSON streaming data to Parquet in S3" → **Firehose with format conversion**
- "Transform streaming data before storage" → **Firehose + Lambda**
- "No code conversion to columnar format" → **Firehose format conversion**

---

## Key Takeaway

> Firehose can transform data with Lambda and convert JSON to Parquet/ORC automatically using the Glue Data Catalog. This is the easiest way to get streaming data into S3 in a query-optimized format.

---

**Previous:** [Firehose Delivery Streams](./08-Firehose-Delivery-Streams.md)
**Next:** [Firehose Buffering](./10-Firehose-Buffering.md)
