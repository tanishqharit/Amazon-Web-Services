# Kinesis Data Firehose Overview

## What is Kinesis Data Firehose?

**Kinesis Data Firehose** is the easiest way to **deliver streaming data** to destinations like S3, Redshift, or OpenSearch. It's fully managed — no coding needed.

---

## How It Works

```
Data Sources → Firehose → (optional transform) → Destination
```

Firehose **buffers** incoming data and delivers it in batches.

---

## Key Destinations

| Destination | Use Case |
|-------------|----------|
| **Amazon S3** | Store streaming data in data lake |
| **Amazon Redshift** | Load into data warehouse (via S3) |
| **Amazon OpenSearch** | Search and analytics |
| **Splunk** | Log analysis |
| **HTTP endpoints** | Custom destinations |

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Fully managed** | No servers, no shards to manage |
| **Near-real-time** | Delivers in batches (60 sec minimum buffer) |
| **Auto-scaling** | Scales automatically |
| **Data transformation** | Can invoke Lambda to transform data |
| **Format conversion** | Can convert JSON → Parquet/ORC automatically |
| **Compression** | Can compress (GZIP, Snappy, etc.) |

---

## Important: Near-Real-Time, NOT Real-Time

Firehose buffers data before delivery:
- **Buffer size:** 1 MB to 128 MB
- **Buffer time:** 60 seconds to 900 seconds

Whichever condition is met first triggers delivery.

---

## Key Takeaway

> Firehose delivers streaming data to S3, Redshift, OpenSearch without managing servers. It's near-real-time (buffered). Can transform data with Lambda and convert to Parquet automatically.

---

**Previous:** [Kinesis Consumers](./06-Kinesis-Consumers.md)
**Next:** [Firehose Delivery Streams](./08-Firehose-Delivery-Streams.md)
